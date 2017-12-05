## Objective-C 算术运算符

下表列出了所有支持Objective-C语言的算术运算符。假设变量A=10和变量B=20，则：
<table>
  <tr>
    <th>运算符</th>
    <th>描述</th>
    <th>示例</th>
  </tr>
  <tr>
    <th>+</th>
    <th>Adds two operands	</th>
    <th>A + B = 30
</th>
  </tr>
  <tr>
    <th>-</th>
    <th>Subtracts second operand from the first	</th>
    <th>A - B = -10</th>
  </tr>
  <tr>
    <th>*</th>
    <th>Multiplies both operands</th>
    <th>A * B = 200</th>
  </tr>
  <tr>
    <th>/</th>
    <th>Divides numerator by denominator</th>
    <th>B / A = 2
</th>
  </tr>
  <tr>
    <th>%</th>
    <th>Modulus Operator and remainder of after an integer division	</th>
    <th>B % A = 0</th>
  </tr>
  <tr>
    <th>++</th>
    <th>Increments operator increases integer value by one	</th>
    <th>A++ = 11</th>
  </tr>
  <tr>
    <th>--</th>
    <th>Decrements operator decreases integer value by one</th>
    <th>A-- = 9</th>
  </tr>
</table>

#### 例子
尝试下面的例子就明白了在Objective-C编程语言的所有算术运算符：
```objc
#import <Foundation/Foundation.h>

main()
{
   int a = 21;
   int b = 10;
   int c ;

   c = a + b;
   NSLog(@"Line 1 - Value of c is %d
", c );
   c = a - b;
   NSLog(@"Line 2 - Value of c is %d
", c );
   c = a * b;
   NSLog(@"Line 3 - Value of c is %d
", c );
   c = a / b;
   NSLog(@"Line 4 - Value of c is %d
", c );
   c = a % b;
   NSLog(@"Line 5 - Value of c is %d
", c );
   c = a++; 
   NSLog(@"Line 6 - Value of c is %d
", c );
   c = a--; 
   NSLog(@"Line 7 - Value of c is %d
", c );

}
```
当编译和执行上述程序，它会产生以下结果：
2017-12-01 22:10:27.005 demo[25774] Line 1 - Value of c is 31
2017-12-01 22:10:27.005 demo[25774] Line 2 - Value of c is 11
2017-12-01 22:10:27.005 demo[25774] Line 3 - Value of c is 210
2017-12-01 22:10:27.005 demo[25774] Line 4 - Value of c is 2
2017-12-01 22:10:27.005 demo[25774] Line 5 - Value of c is 1
2017-12-01 22:10:27.005 demo[25774] Line 6 - Value of c is 21
2017-12-01 22:10:27.005 demo[25774] Line 7 - Value of c is 22