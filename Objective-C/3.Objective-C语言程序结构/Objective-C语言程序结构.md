## Objective-C语言程序结构

在我们研究 Objective-C编程语言的基本构建块之前，让我们来看看一个最起码的 Objective-C程序结构，使我们可以把它作为一个参考接下来的章节中。

#### Objective-C Hello World 示例
一个Objective-C语言程序基本上由以下几部分组成：
- 预处理命令
- 接口
- 实现
- 方法
- 变量
- 语句和表达式
- 注释

让我们看一个简单的代码，将打印词语 "Hello World":
```objc
#import <Foundation/Foundation.h>

@interface SampleClass:NSObject
- (void)sampleMethod;
@end

@implementation SampleClass

- (void)sampleMethod{
   NSLog(@"Hello, World! 
");
}

@end

int main()
{
   /* my first program in Objective-C */
   SampleClass *sampleClass = [[SampleClass alloc]init];
   [sampleClass sampleMethod];
   return 0;
}
```
让我们来看看上述程序的各个部分：
- 程序的第一行 `#import <Foundation/Foundation.h> `是一个预处理命令，它告诉Objective-C语言编译器去实际编译之前包含Foundation.h文件。
- `@interface SampleClass:NSObject` 显示了如何创建一个接口。它继承NSObject，这是所有对象的基类。
- `- (void)sampleMethod; shows how to declare a method `
- `@end` 标志着接口的结束。
- `@implementation SampleClass` 显示如何实现接口`SampleClass
- `- (void)sampleMethod{}` 显示方法 sampleMethod 的实现。
- `@end`标志着实现的结束。
- `int main()` 是主函数在程序开始执行.
- `/*...*/` 由编译器将被忽略，它已经把在程序中添加额外的注释。因此，这样的行称为程序中的注释。
- `NSLog(...)` 另外一个函数可以在Objective-C会打印消息 `“Hello, World!”` 要显示在屏幕上。
- `return 0;` 终止main()函数返回值为0。

#### 编译和执行的Objective-C程序：
现在，当我们编译并运行程序，我们会得到以下的结果。
`2017-11-18 22:38:27.932 learnDemo[28001] Hello, World!`