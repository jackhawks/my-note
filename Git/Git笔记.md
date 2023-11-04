# Git 学习笔记



## 一、Git 操作



### 1. Git 初始化配置



#### (1) 配置内容



**/etc/gitconfig 文件：系统对所有用户都普遍适用的配置。若使用 git config 时用 --system 选项，读写的就是这个文件。**

**~/.gitconfig 文件：用户目录下的配置文件只适用于该用户。若使用 git config 时用 --global 选项，读写的就是这个文件。**

**.git/config 文件：当前项目的 Git 目录中的配置文件（也就是工作目录中的 .git/config 文件）这里的配置仅仅针对当前项目有效。**



> 每个级别都会覆盖上层的相同配置



##### a.用户信息

```shell
# 配置用户名
git config --global user.name "jack"

# 配置 Email
git config --global user.email "jack@xxx.com"

# 查看配置列表
git config --list
```



### 2.底层概念（底层命令）



#### (1) 初始化新仓库

```shell
git init
```



#### (2) .git 目录

```shell
-rw-r--r-- 1 alex 197609  23 Oct 26 00:16 HEAD
-rw-r--r-- 1 alex 197609 130 Oct 26 00:16 config
-rw-r--r-- 1 alex 197609  73 Oct 26 00:16 description
drwxr-xr-x 1 alex 197609   0 Oct 26 00:16 hooks/
drwxr-xr-x 1 alex 197609   0 Oct 26 00:16 info/
drwxr-xr-x 1 alex 197609   0 Oct 26 00:16 objects/
drwxr-xr-x 1 alex 197609   0 Oct 26 00:16 refs/
```

|    名称     |    类型    | 解释                                     |
| :---------: | :--------: | ---------------------------------------- |
|    hooks    |   文件夹   | 包含客户端或服务端的钩子脚本             |
|    info     |   文件夹   | 包含一个全局性的排除文件                 |
| **objects** | **文件夹** | **存储所有数据内容**                     |
|  **refs**   | **文件夹** | **存储指向数据（分支）的提交对象的指针** |
|   config    |    文件    | 包含项目特有的配置选项                   |
| description |    文件    | 用来显示对仓库的描述信息                 |
|  **HEAD**   |  **文件**  | **指示目前被检出的分支**                 |
|  **index**  |  **文件**  | **保存暂存区的信息**                     |



#### (3) git 对象

Git 的核心部分是一个简单的键值对数据库。你可以向该数据库插入任意类型的内容，它会返回一个键值，通过该键值可以在任意时刻再次检索该内容。

这个键值对在 Git 内部是一个 blob 类型。



##### a.向数据库写入内容，并返回对应的键值

命令：

```shell
echo 'hello world' | git hash-object -w --stdin

# 命令注释
-w	选项指示	hash-object	命令存储数据对象；若不指定此项，则该命令仅返回对应的键值
--stdin(standard input)	选项则指示该命令从标准输入读取内容；若不指定该项，则需要在命令尾部给出待输出文件的路径


git hash-object -w [文件路径] # 存文件

git hash-object [文件路径] # 返回对应文件的键值
3b18e512dba79e4c8300dd08aeb37f8e728b8dad
```



返回：

该命令输出一个长度为 40 个字符的校验和。这是一个 SHA-1 哈希值。



##### b.查看 Git 是如何存储数据的

命令：

```shell
find .git/objects -type f
```



返回：

```shell
.git/objects/3b/18e512dba79e4c8300dd08aeb37f8e728b8dad
```

这就是开始时 Git 存储内容的方式：一个文件对应一条内容。校验和的前 2 个字符用于命名子目录，剩下的 38 个字符则用作文件名。



##### c.根据键值拉取数据

命令：

```shell
git cat-file -p 3b18e512dba79e4c8300dd08aeb37f8e728b8dad

# 命令注释
-p 该选项自动判断内容类型，并显示友好的内容
```



返回：

对应文件的内容



#### (4) 对一个文件进行简单的版本控制



##### a.创建一个新文件并将其内容存入数据库

命令：

```shell
echo 'hello world v1' > test.txt
git hash-object -w test.txt
```



返回：

```shell
1730b7818411ba9c2bcb5a5ed48ec0712bf7968c
```



##### b.向文件里写入新的内容，并再次将其存入数据库

命令：

```shell
echo 'hello world v2' > test.txt
git hash-object -w test.txt
```



返回：

```shell
2f33cff919718a9b083f7b20beeacbf04c3f04e5
```



##### c.查看数据库内容

命令：

```shell
find .git/objects -type f

# 查看文件内容
git cat-file -p 2f33cff919718a9b083f7b20beeacbf04c3f04e5

# 查看文件类型
git cat-file -t 2f33cff919718a9b083f7b20beeacbf04c3f04e5

#### 利用 -t 选项，可以让 Git 告诉我们其内部存储的对象类型
```



> 注意：
>
> 当前的操作都是对 Git 本地数据库的操作，不涉及暂存区



#### (5) 树对象

树对象（tree object），它能解决文件名保存的问题，也允许我们将多个文件组织到一起，Git 以一种类似于 UNIX 文件系统的方式存储内容。所有内容均以树对象和数据对象（Git 对象）的形式存储，其中树对象对应了 UNIX 中的目录项，数据对象（Git 对象）则大致上对应文件内容。一个树对象包含了一条或多条记录（每条记录包含一个指向 Git 对象或者子树对象的 SHA-1 指针），以及相应的模式、类型、文件名信息）。一个树对象也可以包含另一个树对象。



##### a.查看树对象

命令：

```shell
git cat-file -p master^{tree}
```



返回：



#### (6) 构建树对象

我们可以通过 update-index，write-tree，read-tree 等命令来构建树对象并塞入到暂存区。



##### a.操作



























 

