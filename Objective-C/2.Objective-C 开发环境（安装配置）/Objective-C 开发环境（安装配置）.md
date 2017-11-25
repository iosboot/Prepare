## Objective-C 开发环境（安装配置）

#### 开发环境设置
如果你愿意设立Objective-C编程语言环境，需要以下两个软件可在您的电脑上：文字编辑器及GCC编译器。

#### 文本编辑器
这将用于编写程序。包括，操作系统Windows记事本编辑命令，Epsilon，Emacs和vim或vi。

文本编辑器的名称和版本，可以在不同的操作系统而异。例如，记事本将在Windows上使用，vim或VI可用于在Windows以及Linux/UNIX。

创建的文件编辑器被称为源文件和包含的源代码程序。 Objective-C程序的源文件通常命名的扩展名为 ".m".

在开始编程之前，确保你有一个文本编辑器地点和经验来写计算机程序，将它保存在一个文件中，编译它，并最终执行

#### GCC编译器
在源文件中编写的源代码，程序是人类可读的源代码。它需要被“编译”转成机器语言，让你的CPU能够实际执行程序每个指令。

此GCC编译器将用于源代码编译成最终的可执行程序。假定你已有了解一个编程语言编译器的基本知识。

GCC编译器可在各种平台和设立各种平台上的程序说明如下。

#### UNIX/Linux上安装
最初的步骤是用gcc的Objective-C包安装gcc。这是通过：
```
$ su - 
$ yum install gcc
$ yum install gcc-objc
```
下一步是设立软件包的依赖关系，使用下面的命令：
```
$ yum install make libpng libpng-devel libtiff libtiff-devel libobjc libxml2 libxml2-devel libX11-devel libXt-devel libjpeg libjpeg-devel
```
为了得到Objective-C的全部功能，请下载并安装GNUstep。这可以通过从下载包 http://main.gnustep.org/resources/downloads.php.

现在，我们需要切换到下载的文件夹，解压缩文件：
```
$ tar xvfz gnustep-startup-.tar.gz
```
现在，我们需要切换到GNUstep的启动文件夹被创建：
```
$ cd gnustep-startup-
```
接下来，我们需要配置的构建过程：
```
$ ./configure
```
然后，我们可以构建：
```
$ make
```
我们最后设置环境
```
$ . /usr/GNUstep/System/Library/Makefiles/GNUstep.sh
```
我们有一个helloWorld.m的Objective-C程序如下：
```objc
#import <Foundation/Foundation.h>

int main (int argc, const char * argv[])
{
    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];
    NSLog (@"hello world");
    [pool drain];
    return 0;
}
```
现在，我们可以编译和运行一个Objective-C 文件为 helloWorld.m 切换到使用 cd 进入文件夹中包含的文件，然后使用以下步骤：
```
$ gcc `gnustep-config --objc-flags` -L/usr/GNUstep/Local/Library/Libraries -lgnustep-base helloWorld.m -o helloWorld
$ ./helloWorld
```
我们可以看到下面的输出
```
2017-11-17 12:23:19.521 learnDemo[12906] hello world
```

#### 在Mac OS上安装
如果使用的是Mac OS X，最简单的方式获得GCC是从苹果公司的网站下载Xcode开发环境，并按照简单的安装说明。一旦有Xcode 将能够使用GNU编译C/C + +。

Xcode目前可用在下列链接： developer.apple.com/technologies/tools/.

#### 在Windows上安装
为了运行的Objective-C程序在Windows上，我们需要安装MinGW和GNUstep核心部分的。两者都可以在gnustep.org/experience/Windows.htmll.

首先，我们需要安装MSYS/ MinGW的系统包。我们需要到安装GNUstep 的核心包。这两者提供了一个windows安装程序。

然后使用Objective-C和GNUstep的选择“开始”-> 所有程序 -> GNUstep -> Shell

切换到该文件夹包含 helloWorld.m

我们可以使用编译程序：
```
$ gcc `gnustep-config --objc-flags` -L /GNUstep/System/Library/Libraries hello.m -o hello -lgnustep-base -lobjc
```
我们可以运行程序，使用：
```
./hello.exe
```
我们得到以下的输出：
```
2017-11-17 13:18:21.492 learnDemo[1200] hello world
```