## Objective-C 常量
常数是指为固定值该程序可能不会改变其执行过程中。这些固定的值也被称为文字（ literals）。

常量可以是任何基本的数据类型，如一个浮点常量，整型常量，字符常量，或一个字符串。也有枚举常量。

就像对待常规变量，但不能修改它们的值后其定义的常量。

#### 整数文字
整数文字可以是十进制，八进制或十六进制常量。前缀指定基本或基数：0x或0X为十六进制，八进制为0，并没有小数。

整数文字也可以有一个后缀，即U和L的组合，无符号长分别。后缀可以是大写或小写，并且可以在任何顺序。

下面是整数文字一些例子：
```
212         /* Legal */
215u        /* Legal */
0xFeeL      /* Legal */
078         /* Illegal: 8 is not an octal digit */
032UU       /* Illegal: cannot repeat a suffix */
```
以下是其他各种类型的整数文字的例子：
```
85         /* decimal */
0213       /* octal */
0x4b       /* hexadecimal */
30         /* int */
30u        /* unsigned int */
30l        /* long */
30ul       /* unsigned long */
```

#### 浮点文字
浮点文字的整数部分，小数点，小数部分和指数部分。可以表示浮点文字小数形式或指数形式。

虽然表示使用十进制的形式，必须包括小数点，指数，或两者同时表示使用指数形式时，必须包括的整数部分，小数部分，或两者。签署指数引入e或E。

下面是浮点文字一些例子：
```
3.14159       /* Legal */
314159E-5L    /* Legal */
510E          /* Illegal: incomplete exponent */
210f          /* Illegal: no decimal or exponent */
.e55          /* Illegal: missing integer or fraction */
```

#### 字符常量
字符文本括在单引号，如'X'，并且可以存储在一个简单的char型变量。

字符文字，可以是一个普通的字符（例如，'X'），转义序列（例如，'	'），或通用字符（例如，“ u02C0'的）。

有一定的字符在C被加一个反斜杠有特殊的意义，它们被用来表示类似的换行符（ ）或制表符（	）。在这里，有一些这样的转义序列代码的列表：
<table>
  <tr>
    <th>转义序列</th>
    <th>意思</th>
  <tr>
  <tr>
    <th></th>
    <th>character</th>
  <tr>
  <tr>
    <th>'</th>
    <th>' character</th>
  <tr>
  <tr>
    <th>"</th>
    <th>" character</th>
  <tr>
  <tr>
    <th>?</th>
    <th>? character</th>
  <tr>
  <tr>
    <th>a</th>
    <th>Alert or bell</th>
  <tr>
  <tr>
    <th></th>
    <th>Backspace</th>
  <tr>
  <tr>
    <th>f</th>
    <th>Form feed</th>
  <tr>
  <tr>
    <th></th>
    <th>Newline</th>
  <tr>
  <tr>
    <th></th>
    <th>Carriage return</th>
  <tr>
  <tr>
    <th></th>
    <th>Horizontal tab</th>
  <tr>
  <tr>
    <th>v</th>
    <th>Vertical tab</th>
  <tr>
  <tr>
    <th>ooo</th>
    <th>Octal number of one to three digits</th>
  <tr>
  <tr>
    <th>xh...</th>
    <th>Hexadecimal number of one or more digits</th>
  <tr>
</table>
下面的例子显示一些字符转义序列：
```objc
#import <Foundation/Foundation.h>

int main()
{
   NSLog(@"Hello	World

");

   return 0;
}
```
上面的代码编译和执行时，它会产生以下结果：
```
2017-12-01 22:17:17.923 demo[17871] Hello	World
```

#### 字符串文字
文字或常量字符串括在双引号“”。一个字符串包含的字符，字符文字：普通字符，转义序列和通用字符相似。

可以打破一个长行，使用字符串和使用空格把它们分开成多行。

下面是一些例子字符串常量。所有三种形式是相同的字符串。
```
"hello, dear"

"hello, 

dear"

"hello, " "d" "ear"
```

#### 定义常量
有两种简单的方法来定义常量在C中：
- 使用 #define 预处理.
- 使用const 关键字.

#### #define 预处理
以下是使用＃define预处理定义一个常数的形式：
```objc
#define identifier value
```
以下举例说明它的细节：
```objc
#import <Foundation/Foundation.h>

#define LENGTH 10   
#define WIDTH  5
#define NEWLINE '
'

int main()
{

   int area;  
  
   area = LENGTH * WIDTH;
   NSLog(@"value of area : %d", area);
   NSLog(@"%c", NEWLINE);

   return 0;
}
```
上面的代码编译和执行时，它会产生以下结果：
```
2017-12-01 22:18:16.637 demo[21460] value of area : 50
2017-12-01 22:18:16.638 demo[21460] 
```

#### const 关键字
可以使用const 来声明常量的前缀与特定类型如下：
```
const type variable = value;
```
以下举例说明它的细节：
```objc
#import <Foundation/Foundation.h>

int main()
{
   const int  LENGTH = 10;
   const int  WIDTH  = 5;
   const char NEWLINE = '
';
   int area;  
   
   area = LENGTH * WIDTH;
   NSLog(@"value of area : %d", area);
   NSLog(@"%c", NEWLINE);

   return 0;
}
```
上面的代码编译和执行时，它会产生以下结果：
```
2017-12-01 22:19:24.780 demo[25621] value of area : 50
2017-12-01 22:19:24.781 demo[25621] 
```
请注意，这是一个良好的编程习惯来定义常量 CAPITALS.