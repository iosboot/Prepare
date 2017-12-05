## Objective-C 逻辑运算符
下表列出了所有支持Objective-C语言的逻辑运算符。假设变量A=1，变量B=0，那么：
<table>
  <tr>
    <th>运算符</th>
    <th>描述</th>
    <th>示例</th>
  </tr>
  <tr>
    <th>&&</th>
    <th>调用逻辑AND运算符。如果这两个操作数不为零，则条件为真。</th>
    <th>(A && B) is false.</th>
  </tr>
  <tr>
    <th>||</th>
    <th>调用逻辑或运算符。如果两个操作数中的任何一个不为零，则条件为真。</th>
    <th>(A || B) is true.</th>
  </tr>
  <tr>
    <th>!</th>
    <th>调用逻辑NOT运算。使用反转其操作数的逻辑状态。如果一个条件是真的，那么逻辑NOT运算符为假。</th>
    <th>!(A && B) is true.</th>
  </tr>
</table>

#### 示例
尝试下面的例子就明白了所有在Objective-C编程语言的逻辑运算符：
```objc
#import <Foundation/Foundation.h>

main()
{
   int a = 5;
   int b = 20;
   int c ;

   if ( a && b )
   {
      NSLog(@"Line 1 - Condition is true
" );
   }
   if ( a || b )
   {
      NSLog(@"Line 2 - Condition is true
" );
   }
   /* lets change the value of  a and b */
   a = 0;
   b = 10;
   if ( a && b )
   {
      NSLog(@"Line 3 - Condition is true
" );
   }
   else
   {
      NSLog(@"Line 3 - Condition is not true
" );
   }
   if ( !(a && b) )
   {
      NSLog(@"Line 4 - Condition is true
" );
   }
}
```
当编译和执行上述程序，它会产生以下结果：
```
2017-12-05 22:35:57.256 demo[19012] Line 1 - Condition is true
2017-12-05 22:35:57.256 demo[19012] Line 2 - Condition is true
2017-12-05 22:35:57.256 demo[19012] Line 3 - Condition is not true
2017-12-05 22:35:57.256 demo[19012] Line 4 - Condition is true
```