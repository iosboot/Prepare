## Objective-C 数据类型
在Objective-C 编程语言，数据类型是指一个广泛的系统，用于不同类型的声明变量或函数。多少它占据的空间存储和存储的位模式如何被解释变量的类型确定。

Objective-C语言中的类型可分类如下：
<table>
  <tr>
    <th>S.N.</th>
    <th>类型和说明</th>
  </tr>
  <tr>
    <th>1</th>
    <th>基本类型:
它们是算术类型，包括两种类型：（一）的整数类型，及（b）浮点型。</th>
  </tr>
  <tr>
    <th>2</th>
    <th>枚举类型:
也是算术类型，它们被用来定义变量只能被分配在整个程序中的若干离散的整数值。</th>
  </tr>
  <tr>
    <th>3</th>
    <th>void类型:
类型说明符void表示没有可用的值。</th>
  </tr>
  <tr>
    <th>4</th>
    <th>派生类型：
他们包括指针类型，数组类型，结构类型，联合类型及函数类型。</th>
  </tr>
</table>
被称为统称为聚合类型的数组类型和结构类型。一个函数的类型指定函数的返回值的类型。而其他类型将会在即将到来的章节，我们将在下面的章节中看到的基本类型。

#### 整型
下表给出了有关标准的整数类型的存储大小和值范围：
<table>
  <tr>
    <th>类型</th>
    <th>存储长度</th>
    <th>值范围</th>
  </tr>
  <tr>
    <th>char</th>
    <th>1 byte</th>
    <th>-128 to 127 or 0 to 255</th>
  </tr>
  <tr>
    <th>unsigned char</th>
    <th>1 byte</th>
    <th>0 to 255</th>
  </tr>
  <tr>
    <th>signed char</th>
    <th>1 byte</th>
    <th>-128 to 127</th>
  </tr>
  <tr>
    <th>int</th>
    <th>2 or 4 bytes</th>
    <th>-32,768 to 32,767 or -2,147,483,648 to 2,147,483,647</th>
  </tr>
  <tr>
    <th>unsigned int</th>
    <th>2 or 4 bytes</th>
    <th>	0 to 65,535 or 0 to 4,294,967,295</th>
  </tr>
  <tr>
    <th>short</th>
    <th>2 bytes</th>
    <th>-32,768 to 32,767</th>
  </tr>
  <tr>
    <th>unsigned short</th>
    <th>2 bytes</th>
    <th>0 to 65,535</th>
  </tr>
  <tr>
    <th>long</th>
    <th>4 bytes</th>
    <th>-2,147,483,648 to 2,147,483,647</th>
  </tr>
  <tr>
    <th>unsigned long</th>
    <th>4 bytes</th>
    <th>0 to 4,294,967,295
</th>
  </tr>
</table>
为了得到确切的大小，类型或变量在特定平台上，可以使用sizeof运算符。表达式sizeof（类型）产生的对象或类型以字节为单位的存储大小。以下是这个例子中的任何一台机器上的 int类型的大小：
```objc
#import <Foundation/Foundation.h>

int main()
{
   NSLog(@"Storage size for int : %d 
", sizeof(int));
   
   return 0;
}
```
当编译并执行上述程序，在Linux上产生以下结果：
```
2013-09-07 22:21:39.155 demo[1340] Storage size for int : 4 
```

#### 浮点类型
下表给出了有关标准的存储大小和取值范围和精度的浮点类型的详细信息
<table>
  <tr>
    <th>类型</th>
    <th>存储大小</th>
    <th>取值范围</th>
    <th>精确</th>
  </tr>
  <tr>
    <th>float</th>
    <th>4 byte</th>
    <th>1.2E-38 to 3.4E+38</th>
    <th>6 decimal places</th>
  </tr>
  <tr>
    <th>double</th>
    <th>8 byte</th>
    <th>2.3E-308 to 1.7E+308</th>
    <th>15 decimal places</th>
  </tr>
  <tr>
    <th>long double</th>
    <th>10 byte</th>
    <th>3.4E-4932 to 1.1E+4932</th>
    <th>19 decimal places</th>
  </tr>
</table>
头文件float.h中定义的宏，允许使用这些值和其他详细信息在程序中实数的二进制表示。下面的例子将打印存储空间所采取的浮点类型，其范围值：
```objc
#import <Foundation/Foundation.h>

int main()
{
   NSLog(@"Storage size for float : %d 
", sizeof(float));
   
   return 0;
}
```
当编译并执行上述程序，在Linux上产生以下结果：
```
2013-09-07 22:22:21.729 demo[3927] Storage size for float : 4 
```

#### void 类型
void类型指定，没有可用的值。它被用在三种情况：
<table>
  <tr>
    <th>S.N.</th>
    <th>类型和说明</th>
  </tr>
  <tr>
    <th>1</th>
    <th>函数返回为void
Objective-C中有各种不同的函数，对于没有返回值，或者可以说他们返回void。没有返回值的函数的返回类型为void。例如, void exit (int status);</th>
  </tr>
  <tr>
    <th>2</th>
    <th>函数参数为void
Objective-C中有各种不同的函数，不接受任何参数。不带参数的函数可以接受一个void。例如, int rand(void);</th>
  </tr>
</table>
void类型在这一点上可能不很好的理解，让我们继续在接下来的章节中，我们将介绍这些概念