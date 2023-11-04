# CSS 书写规范



### 建议遵循以下顺序

1. **布局定位属性：**display / position / float / clear / visibility / overflow (建议 display 第一个写)
2. **自身属性：**width / height / margin / padding / border / background
3. **文本属性：**color / font / text-decoration / text-align / vertical-align / white-space / break-word
4. **其他属性：**content / cursor / border-redius / box-shadow / text-shadow / background:linear-gradinent.....

> 注意：每个顺序与下一个顺序之间应该空一行



### 页面布局的整体思路

为了提高网页制作的效率，布局时通常有以下的整体思路：

1. 必须确定页面的**版心**（可视区域），可通过测量得出
2. 分析页面中的行模块，以及每个行模块中的列模块（页面的第一准则）
3. 一行中的列模块经常浮动布局，先确定每个列的大小，之后确定列的位置（页面的第二准则）
4. 制作HTML结构，遵循**先有结构，后有样式**的原则（结构永远最重要）
5. 先理清楚**布局结构**，再写代码（这点尤为重要）