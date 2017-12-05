## Objective-C 关系运算符
下表列出了所有支持Objective-C语言的关系运算符。假设变量A=10和变量B=20，则：
<table>
  <tr>
    <th>运算符</th>
    <th>描述</th>
    <th>示例</th>
  </tr>
  <tr>
    <th>==</th>
    <th>检查是否两个操作数的值等于或不等于，如果是的话那么条件为真。</th>
    <th>(A == B) is not true.</th>
  </tr>
  <tr>
    <th>!=</th>
    <th>检查两个操作数的值等于或不相等，如果值不相等，则条件为真</th>
    <th>(A != B) is true.</th>
  </tr>
  <tr>
    <th>></th>
    <th>检查是否左操作数的值大于右操作数的值，如果是的话那么条件为真。</th>
    <th>(A > B) is not true.</th>
  </tr>
  <tr>
    <th><</th>
    <th>检查是否左操作数的值小于右操作数的值，如果是的话那么条件为真。</th>
    <th>A < B) is true.</th>
  </tr>
  <tr>
    <th>>=</th>
    <th>检查是否左操作数的值大于或等于右操作数的值，如果是的话那么条件为真。</th>
    <th>	(A >= B) is not true.</th>
  </tr>
  <tr>
    <th><=</th>
    <th>检查是否左操作数的值小于或等于右边的操作数的值，如果是的话那么条件为真。</th>
    <th>(A <= B) is true.</th>
  </tr>
</table>

#### 例子
尝试下面的例子就明白了在Objective-C编程语言的所有关系运算符：
```objc
#import <Foundation/Foundation.h>

main()
{
   int a = 21;
   int b = 10;
   int c ;

   if( a == b )
   {
      NSLog(@"Line 1 - a is equal to b
" );
   }
   else
   {
      NSLog(@"Line 1 - a is not equal to b
" );
   }
   if ( a < b )
   {
      NSLog(@"Line 2 - a is less than b
" );
   }
   else
   {
      NSLog(@"Line 2 - a is not less than b
" );
   }
   if ( a > b )
   {
      NSLog(@"Line 3 - a is greater than b
" );
   }
   else
   {
      NSLog(@"Line 3 - a is not greater than b
" );
   }
   /* Lets change value of a and b */
   a = 5;
   b = 20;
   if ( a <= b )
   {
      NSLog(@"Line 4 - a is either less than or equal to  b
" );
   }
   if ( b >= a )
   {
      NSLog(@"Line 5 - b is either greater than  or equal to b
" );
   }
}
```
当编译和执行上述程序，它会产生以下结果：
```
2017-12-05 22:42:18.254 demo[9486] Line 1 - a is not equal to b
2017-12-05 22:42:18.254 demo[9486] Line 2 - a is not less than b
2017-12-05 22:42:18.254 demo[9486] Line 3 - a is greater than b
2017-12-05 22:42:18.254 demo[9486] Line 4 - a is either less than or equal to  b
2017-12-05 22:42:18.254 demo[9486] Line 5 - b is either greater than  or equal to b
```