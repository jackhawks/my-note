# TL语言

TL（类型语言）用于描述使用的类型系统、构造函数和现有函数。事实上，使用的是[二进制数据序列化中呈现的组合器描述格式。](https://core.telegram.org/mtproto/serialize)

另请参见：

-   [TL中的多态性](https://core.telegram.org/mtproto/TL-polymorph)

高级主题：

-   [TL 中的依赖类型](https://core.telegram.org/mtproto/TL-dependent)
-   [TL的形式化描述](https://core.telegram.org/mtproto/TL-formal)
-   [TL组合器的形式化描述](https://core.telegram.org/mtproto/TL-combinators)
-   [类型序列化](https://core.telegram.org/mtproto/TL-types)
-   [用于 TL 模式序列化的 TL 模式](https://core.telegram.org/mtproto/TL-tl)
-   [可选的组合器参数及其值](https://core.telegram.org/mtproto/TL-optargs)
-   [二进制序列化和抽象 TL 类型](https://core.telegram.org/mtproto/TL-abstract-types)
-   [TL中模板的形式描述](https://core.telegram.org/mtproto/TL-patterns)

### 概述

一个TL程序通常由两部分组成，这两部分由关键字 `---functions---` 分隔。第一部分包含内置类型和聚合类型（即它们的构造器）的声明组成。第二部分包含声明的函数组成，即函数组合器。

实际上，第一部分和第二部分都由组合器声明组成，每个组合器声明都以分号结束。但是，第一部分仅包含构造器函数，而第二部分只涉及函数。每个组合器都使用上面解释的格式进行“组合器声明”。然而，可以显式指定组合器的编号和字段名称。

如果在声明函数之后需要附加额外的类型声明，使用关键字 `---types---` （分隔符）。此外，如果函数组合器的结果类型以感叹号开头（实际上，当函数部分被解释时，这个感叹号会自动添加），则可以在类型部分中声明该函数组合器。

为了显式定义组合器的32位名称，请在组合器名称后面立即添加井号(#)，后跟8个十六进制数字。

### 命名空间

复合结构如 `<namespace_identifier>.<constructor_identifier>` 和 `<namespace_identifier>.<Type_identifier>` 可以用作构造函数或类型标识符。标识符中点左侧的部分被称为*命名空间*。此外，类型标识符首字母大写、构造器标识符首字母小写的规则适用于点之后的部分。例如，`auth.Message `是一个类型，而 `auth.std_message` 是一个构造函数。

命名空间不需要特殊声明。

### 评论

注释与 C++ 中的注释相同。

### 例子

```
// built-in types
int#a8509bda ? = Int;
long ? = Long;
double ? = Double;
string ? = String;
null = Null;

vector {t:Type} # [ t ] = Vector t;
coupleInt {alpha:Type} int alpha = CoupleInt<alpha>;
coupleStr {gamma:Type} string gamma = CoupleStr gamma;  
/* The name of the type variable is irrelevant: "gamma" could be replaced with "alpha"; 
   However, the combinator number will depend on the specific choice. */

intHash {alpha:Type} vector<coupleInt<alpha>> = IntHash<alpha>;
strHash {alpha:Type} (vector (coupleStr alpha)) = StrHash alpha;
intSortedHash {alpha:Type} intHash<alpha> = IntSortedHash<alpha>;
strSortedHash {alpha:Type} (strHash alpha) = StrSortedHash alpha;

// custom types
pair x:Object y:Object = Pair;
triple x:Object y:Object z:Object = Triple;

user#d23c81a3 id:int first_name:string last_name:string = User;
no_user#c67599d1 id:int = User;
group id:int title:string last_name:string = Group;
no_group = Group;

---functions---

// Maybe some built-in arithmetic functions; inverse quotes make "identifiers" out of arbitrary non-alphanumeric strings
`+` Int Int = Int;
`-` Int Int = Int;
`+` Double Double = Double;
// ...

// API functions (aka RPC functions)
getUser#b0f732d5 int = User;
getUsers#2d84d5f5 (Vector int) = Vector User;
```

在这种情况下，`user` 构造函数已被显式的分配了一个数字(0xd23c81a3)；实际上，这不是必需的，因为这个值是 string  `"user id:int first_name:string last_name:string = User"` 的 CRC32，这个值将被默认使用。

对于 Vector int、Vector User、Vector Object 等，不需要特殊的构造器——可以在任何地方使用相同的通用构造器。

```
vector#1cb5c415 {t:Type} # [ t ] = Vector t;
```

请注意，当计算 `getUsers (Vector int) = Vector User;` 构造器编号时，会计算字符串 "getUsers Vector int = Vector User" 的 CRC32（已删除所有括号）。

符号 `T0<T1,T2,...,Tn>` 是 `(T0 (T1) (T2) ... (Tn))` 的语法糖。例如，`Vector<User>`和`(Vector User)`是完全可以互换的。

#### RPC 查询示例

假设我们想要调用 `getUsers([2,3,4])` 。该查询将被序列化为 32 位整数序列，如下所示：

```
0x2d84d5f5 0x1cb5c415 0x3 0x2 0x3 0x4
```

请注意，TL 序列化生成一个 32 位整数序列。当必须将其嵌入字节流（例如网络数据包）时，每个 32 位整数由四个字节以小端序表示。这样，上述查询对应于以下字节流：

```
F5 D5 84 2D 15 C4 B5 1C 03 00 00 00 02 00 00 00 03 00 00 00 04 00 00 00
```

响应可能看起来像这样：

```
0x1cb5c415 0x3 0xd23c81a3 0x2 0x74655005 0x00007265 0x72615006 0x72656b 0xc67599d1 0x3 0xd23c81a3 0x4 0x686f4a04 0x6e 0x656f4403
```

这大致对应于

```
[{"id":2,"first_name":"Peter", "last_name":"Parker"},{},{"id":4,"first_name":"John","last_name":"Doe"}]
```

在这两种情况中，都使用了相同的通用构造器 `vector#1cb5c415` ：在请求序列化类型为 `Vector int` 的值时，以及在响应中序列化类型为 `Vector User` 的值时。这里没有歧义，因为在两种情况下，开始 (反) 序列化之前都已知要处理的值的类型。例如，在接收到查询后，服务器看到第一部分是 `0x2d84d5f5`，这对应于构造器 `getUsers#2d84d5f5 (Vector int) = Vector User` 。因此，它理解接下来将是一个类型为 `Vector int` 的值。在收到此查询的响应后，客户端知道它必须接收一个类型为 `Vector User` 的值，并相应地对响应进行反序列化。

