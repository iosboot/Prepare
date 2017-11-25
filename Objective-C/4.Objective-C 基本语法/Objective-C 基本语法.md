## Objective-C 基本语法
我们在前面已经看到了Objective-C语言程序的基本结构，所以这比较容易理解其他的 Objective-C编程语言的基本构造块。

#### 在Objective-C令牌
Objective-C语言程序包括各种令牌，令牌是一个关键字，一个标识符，常量，字符串文字或符号。例如，下面的语句由Objective-C的6个令牌组成：
```objc
NSLog(@"Hello, World!");
```
单独的标记如下
```objc
NSLog
@
(
"Hello, World! 
"
)
;
```
#### 分号;
在Objective-C程序中，分号是语句终止。也就是说，每一个单独的语句必须以分号结束。表示结束的一个逻辑实体。

例如，下面是两个不同的语句：
```objc
NSLog(@"Hello, World!");
return 0;
```

#### 注释
注释就像Objective-C程序中的文本帮助，它们被编译器忽略。他们开始用/* 和 */如下所示的字符终止：
`/* my first program in Objective-C */
`
不能在注释有注释，他们不会出现在一个字符串或字符文字。

#### 标识符
Objective-C的标识符是用来标识变量，函数，或任何其它用户定义的项目名称。一个标识符开始以字母A到Z或a到z或下划线_后跟零个或多个字母，下划线和数字（0〜9）。

Objective-C中不允许标点符号如@，$，％以内标识符。 Objective-C语言是区分大小写的编程语言。因此，Manpower  和 manpower 在Objective-C是两个不同的标识符。可接受的标识下面是一些例子：
```
mohd       zara    abc   move_name  a_123
myname50   _temp   j     a23b9      retVal
```

#### 关键字
下面的列表显示了一些Objective-C语言中的保留字。这些保留字不能用作常数或变数，或任何其他标识符名称。
<table>
        <tr>
            <th>auto</th>
            <th>else</th>
            <th>long</th>
            <th>switch</th>
        </tr>
        <tr>
            <th>break</th>
            <th>enum</th>
            <th>register</th>
            <th>typedef</th>
        </tr>
        <tr>
            <th>case</th>
            <th>extern</th>
            <th>return</th>
            <th>union</th>
        </tr>
        <tr>
            <th>char</th>
            <th>float</th>
            <th>short</th>
            <th>unsigned</th>
        </tr>
        <tr>
            <th>const</th>
            <th>for</th>
            <th>signed</th>
            <th>void</th>
        </tr>
        <tr>
            <th>continue</th>
            <th>goto</th>
            <th>sizeof</th>
            <th>volatile</th>
        </tr>
        <tr>
            <th>default</th>
            <th>if</th>
            <th>static</th>
            <th>while</th>
        </tr>
        <tr>
            <th>do</th>
            <th>int</th>
            <th>struct</th>
            <th>_Packed</th>
        </tr>
        <tr>
            <th>double</th>
            <th>protocol</th>
            <th>interface</th>
            <th>implementation</th>
        </tr>
        <tr>
            <th>NSObject</th>
            <th>NSInteger</th>
            <th>NSNumber</th>
            <th>CGFloat</th>
        </tr>
        <tr>
            <th>property</th>
            <th>nonatomic</th>
            <th>retain</th>
            <th>strong</th>
        </tr>
        <tr>
            <th>weak</th>
            <th>unsafe_unretained</th>
            <th>readwrite</th>
            <th>readonly</th>
        </tr>
</table>

#### Objective-C中的空白
一行只含有空格，可能带有注释，被称为一个空行, Objective-C编译器完全忽略它。

空白是Objective-C中使用的术语来形容空格，制表符，换行符和注释。空白的声明从另一个分离的一部分，使编译器识别一个元件在一份声明中，如int，结束和下一个元素开始。因此，在下面的语句：
```
int age;
```
必须有至少一个int和 age 编译器能够区分它们之间的空白字符（通常是一个空间）。如下语句：
```
fruit = apples + oranges;   // get the total fruit
```
没有空格字符之间 fruit 和=，=和apples之间是必要的。