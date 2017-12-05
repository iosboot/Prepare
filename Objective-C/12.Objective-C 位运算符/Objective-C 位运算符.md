## Objective-C 位运算符
下表中列出了支持Objective-C语言的位运算符。假设变量A=60和变量B=13，则：
<table>
  <tr>
    <th>运算符</th>
    <th>描述说明</th>
    <th>示例</th>
  </tr>
  <tr>
    <th>&</th>
    <th>Binary AND Operator copies a bit to the result if it exists in both operands.</th>
    <th>(A & B) will give 12, which is 0000 1100</th>
  </tr>
  <tr>
    <th>|</th>
    <th>Binary OR Operator copies a bit if it exists in either operand.</th>
    <th>(A | B) will give 61, which is 0011 1101</th>
  </tr>
  <tr>
    <th>^</th>
    <th>Binary XOR Operator copies the bit if it is set in one operand but not both.</th>
    <th>(A ^ B) will give 49, which is 0011 0001</th>
  </tr>
  <tr>
    <th>~</th>
    <th>Binary Ones Complement Operator is unary and has the effect of 'flipping' bits.</th>
    <th>(~A ) will give -61, which is 1100 0011 in 2's complement form due to a signed binary number.</th>
  </tr>
  <tr>
    <th><<</th>
    <th>Binary Left Shift Operator. The left operand's value is moved left by the number of bits specified by the right operand.</th>
    <th>A << 2 will give 240, which is 1111 0000</th>
  </tr>
  <tr>
    <th>>></th>
    <th>Binary Right Shift Operator. The left operand's value is moved right by the number of bits specified by the right operand.</th>
    <th>A >> 2 will give 15, which is 0000 1111</th>
  </tr>
</table>

#### 例子
尝试下面的例子就明白了所有在Objective-C编程语言的位运算符：
```objc
#import <Foundation/Foundation.h>

main()
{

   unsigned int a = 60;	/* 60 = 0011 1100 */  
   unsigned int b = 13;	/* 13 = 0000 1101 */
   int c = 0;           

   c = a & b;       /* 12 = 0000 1100 */ 
   NSLog(@"Line 1 - Value of c is %d
", c );

   c = a | b;       /* 61 = 0011 1101 */
   NSLog(@"Line 2 - Value of c is %d
", c );

   c = a ^ b;       /* 49 = 0011 0001 */
   NSLog(@"Line 3 - Value of c is %d
", c );

   c = ~a;          /*-61 = 1100 0011 */
   NSLog(@"Line 4 - Value of c is %d
", c );

   c = a << 2;     /* 240 = 1111 0000 */
   NSLog(@"Line 5 - Value of c is %d
", c );

   c = a >> 2;     /* 15 = 0000 1111 */
   NSLog(@"Line 6 - Value of c is %d
", c );
}
```
当编译和执行上述程序，它会产生以下结果：
```
2017-12-05 22:11:51.652 demo[30836] Line 1 - Value of c is 12
2017-12-05 22:11:51.652 demo[30836] Line 2 - Value of c is 61
2017-12-05 22:11:51.652 demo[30836] Line 3 - Value of c is 49
2017-12-05 22:11:51.652 demo[30836] Line 4 - Value of c is -61
2017-12-05 22:11:51.652 demo[30836] Line 5 - Value of c is 240
2017-12-05 22:11:51.652 demo[30836] Line 6 - Value of c is 15
```