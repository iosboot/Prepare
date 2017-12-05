## Objective-C 赋值运算符
<table>
  <tr>
    <th>运算符</th>
    <th>描述说明</th>
    <th>示例</th>
  </tr>
  <tr>
    <th>=</th>
    <th>Simple assignment operator, Assigns values from right side operands to left side operand</th>
    <th>C = A + B will assign value of A + B into C</th>
  </tr>
  <tr>
    <th>+=</th>
    <th>Add AND assignment operator, It adds right operand to the left operand and assigns the result to left operand</th>
    <th>C += A 等同于 C = C + A</th>
  </tr>
  <tr>
    <th>-=</th>
    <th>Subtract AND assignment operator, It subtracts right operand from the left operand and assigns the result to left operand</th>
    <th>C -= A 等同于 C = C - A</th>
  </tr>
  <tr>
    <th>*=</th>
    <th>Multiply AND assignment operator, It multiplies right operand with the left operand and assigns the result to left operand</th>
    <th>C *= A 等同于 C = C * A</th>
  </tr>
  <tr>
    <th>/=</th>
    <th>Divide AND assignment operator, It divides left operand with the right operand and assigns the result to left operand</th>
    <th>C /= A 等同于 C = C / A</th>
  </tr>
  <tr>
    <th>%=</th>
    <th>Modulus AND assignment operator, It takes modulus using two operands and assigns the result to left operand</th>
    <th>C %= 等同于 C = C % A</th>
  </tr>
  <tr>
    <th><<=</th>
    <th>Left shift AND assignment operator</th>
    <th>C <<= 2 等同于 C = C << 2</th>
  </tr>
  <tr>
    <th>>>=</th>
    <th>Right shift AND assignment operator</th>
    <th>C >>= 2 等同于 C = C >> 2</th>
  </tr>
  <tr>
    <th>&=</th>
    <th>Bitwise AND assignment operator</th>
    <th>C &= 2 等同于C = C & 2</th>
  </tr>
  <tr>
    <th>^=</th>
    <th>bitwise exclusive OR and assignment operator</th>
    <th>C ^= 2 等同于C = C ^ 2</th>
  </tr>
  <tr>
    <th>!=</th>
    <th>bitwise inclusive OR and assignment operator</th>
    <th>C |= 2 等同于 C = C | 2</th>
  </tr>
</table>

#### 例子
尝试下面的例子就明白了所有在Objective-C编程语言的赋值运算符：
```objc
#import <Foundation/Foundation.h>

main()
{
   int a = 21;
   int c ;

   c =  a;
   NSLog(@"Line 1 - =  Operator Example, Value of c = %d
", c );

   c +=  a;
   NSLog(@"Line 2 - += Operator Example, Value of c = %d
", c );

   c -=  a;
   NSLog(@"Line 3 - -= Operator Example, Value of c = %d
", c );

   c *=  a;
   NSLog(@"Line 4 - *= Operator Example, Value of c = %d
", c );

   c /=  a;
   NSLog(@"Line 5 - /= Operator Example, Value of c = %d
", c );

   c  = 200;
   c %=  a;
   NSLog(@"Line 6 - %= Operator Example, Value of c = %d
", c );

   c <<=  2;
   NSLog(@"Line 7 - <<= Operator Example, Value of c = %d
", c );

   c >>=  2;
   NSLog(@"Line 8 - >>= Operator Example, Value of c = %d
", c );

   c &=  2;
   NSLog(@"Line 9 - &= Operator Example, Value of c = %d
", c );

   c ^=  2;
   NSLog(@"Line 10 - ^= Operator Example, Value of c = %d
", c );

   c |=  2;
   NSLog(@"Line 11 - |= Operator Example, Value of c = %d
", c );

}
```
当编译和执行上述程序，它会产生以下结果：
2017-12-05 22:00:19.263 demo[21858] Line 1 - =  Operator Example, Value of c = 21
2017-12-05 22:00:19.263 demo[21858] Line 2 - += Operator Example, Value of c = 42
2017-12-05 22:00:19.263 demo[21858] Line 3 - -= Operator Example, Value of c = 21
2017-12-05 22:00:19.263 demo[21858] Line 4 - *= Operator Example, Value of c = 441
2017-12-05 22:00:19.263 demo[21858] Line 5 - /= Operator Example, Value of c = 21
2017-12-05 22:00:19.264 demo[21858] Line 6 - %= Operator Example, Value of c = 11
2017-12-05 22:00:19.264 demo[21858] Line 7 - <<= Operator Example, Value of c = 44
2017-12-05 22:00:19.264 demo[21858] Line 8 - >>= Operator Example, Value of c = 11
2017-12-05 22:00:19.264 demo[21858] Line 9 - &= Operator Example, Value of c = 2
2017-12-05 22:00:19.264 demo[21858] Line 10 - ^= Operator Example, Value of c = 0
2017-12-05 22:00:19.264 demo[21858] Line 11 - |= Operator Example, Value of c = 2