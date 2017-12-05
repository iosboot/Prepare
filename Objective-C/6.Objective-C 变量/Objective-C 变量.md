## Objective-C 变量
变量是只不过是一个名字到存储区域，让程序可以操纵。 Objective-C中的每一个变量有特定的类型，确定该变量的存储器的大小和布局，可以存储在该存储器内的值的范围内;和设定操作，可变化应用。

一个变量名可以由字母，数字和下划线。它必须以字母或下划线开始。大写和小写字母是不同的，因为Objective-C语言是区分大小写的。前面的章节中介绍的基本类型的基础上，有以下基本变量类型：
<table>
  <tr>
    <th>类型</th>
    <th>描述</th>
  </tr>
  <tr>
    <th>char</th>
    <th>通常一个单字节（一个字节）。这是一个整数类型.</th>
  </tr>
  <tr>
    <th>int</th>
    <th>机器的自然整数大小.</th>
  </tr>
  <tr>
    <th>float</th>
    <th>单精度浮点值.</th>
  </tr>
  <tr>
    <th>double</th>
    <th>双精度浮点值.</th>
  </tr>
  <tr>
    <th>void</th>
    <th>表示类型没有（空）.</th>
  </tr>
</table>
Objective-C的编程语言还可以定义各种其他类型的变量，我们将在随后的章节，如枚举，指针，数组，结构，联合，对于本章，我们只学习基本的变量类型

#### Objective-C中的变量定义:
定义一个变量意味着告诉编译器在哪里以及如何创建存储变量。一个变量的定义指定了数据类型，并包含一个列表中的一个或多个变量的那类型，如下所示：
```
type variable_list;
```
在这里，type 必须是一个有效的Objective-C 数据类型，包括char，w_char, int, float, double, bool或任何用户定义的对象等，并variable_list 可能包含一个或多个以逗号分隔的标识符名称。一些有效的声明如下所示：
```
int    i, j, k;
char   c, ch;
float  f, salary;
double d;
```
行中 int i, j, k;;声明和定义变量i，j和k指示编译器来创建命名的变量类型为int i，j和k的。

变量可以在他们的声明中初始化（分配一个初始值）。初始化由等号后面的常量表达式如下：
```
type variable_name = value;
```
一些例子：
```
extern int d = 3, f = 5;    // declaration of d and f. 
int d = 3, f = 5;           // definition and initializing d and f. 
byte z = 22;                // definition and initializes z. 
char x = 'x';               // the variable x has the value 'x'.
```
对于没有初始化的定义：具有静态存储持续时间的变量隐式初始化NULL（所有字节值0）;所有其他变量的初始值是不确定的。

#### Objective-C中的变量声明：
变量声明提供编译器，保证有一个具有给定类型和名称的变量，无需完整的细节进行进一步编译，这样编译器存在的变量。变量声明有其意义，编译器在编译的时候只需要在链接程序的时候，实际的变量声明。

当您使用多个文件和你的文件，这将是在链接程序的时候定义的变量，变量声明是有用的。在任何地方，将使用extern关键字来声明一个变量。虽然你可以在你的Objective-C程序中声明一个变量多次，但它可以在文件中，一个函数或代码块中只定义一次。

#### 例子
试试下面的例子中，变量已被定义在顶部，但他们已经定义并初始化里面的主要功能：
```objc
#import <Foundation/Foundation.h>

// Variable declaration:
extern int a, b;
extern int c;
extern float f;

int main ()
{
  /* variable definition: */
  int a, b;
  int c;
  float f;
 
  /* actual initialization */
  a = 10;
  b = 20;
  
  c = a + b;
  NSLog(@"value of c : %d 
", c);

  f = 70.0/3.0;
  NSLog(@"value of f : %f 
", f);
 
  return 0;
}
```
上面的代码编译和执行时，它会产生以下结果：
```
2017-11-29 22:43:31.695 demo[14019] value of c : 30 
2017-11-29 22:43:31.695 demo[14019] value of f : 23.333334 
```
同样的概念适用于函数声明提供在其声明的时候，它的实际定义一个函数名可以给其他地方。在下面的例子，它使用C函数，正如所知道的 Objective-C支持C风格的函数也解释：
```objc
// function declaration
int func();

int main()
{
    // function call
    int i = func();
}

// function definition
int func()
{
    return 0;
}
```

#### Objective-C中的左值和右值：
Objective-C中有两种类型的表达式：

- lvalue : 该表达式是一个左值，可能会出现一个赋值为左边或右边。

- rvalue : 这是一个右值表达式可能会出现在右侧而不是左侧的任务。

变量是左值，可能会出现在左手侧的一个赋值。数字文本是右值，所以不得指让，并不能出现在左侧。以下是一个有效的语句：
```
int g = 20;
```
但是，下面不是一个有效的语句，会产生编译时错误：
```
10 = 20;
```