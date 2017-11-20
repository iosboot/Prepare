# 安装 WordPress

前期没有购买服务器，需要本地安装WordPress

## 服务器环境要求
- PHP 5.2.4或更新版本
- MySQL 5.0或更新版本
- Apache mod_rewrite模块（可选，用于支持“固定链接”和“站点网络”功能）

## 使用MAMP在Mac上本地安装WordPress

### 什么是MAMP
MAMP代表Macintosh，Apache，MySQL和PHP。MAMP是一个可以在Mac上安装的应用程序，它允许您访问本地PHP服务器和MySQL服务器。 从本质上讲，MAMP为您提供了在您的机器上运行WordPress所需的所有工具，用于开发和测试目的。

### 安装MAMP步骤

1. 安装MAMP：在Mac上安装MAMP之前，您需要从MAMP网站上下载它。 MAMP要求您的Mac运行Mac OS X 10.6.6或更高版本。  
MAMP破解版[下载地址](https://waitsun.ctfile.com/fs/160721-223409240)

2. 基本的MAMP设置：启动MAMP,在编辑设置时，MAMP可能会提示您输入管理员密码。 这是必需的，因为MAMP需要运行两个进程：mysqld（MySQL）和httpd（Apache）。一旦你打开MAMP，点击Preferences。 接下来点击“Ports”。 Apache的默认MAMP端口为8888，MySQL为8889。 如果你使用这个配置，你不应该被要求输入密码，但是你需要在URL（localhost：8888）中包含端口号。 如果您希望将端口号从URL中删除，请将Apache端口更改为80.使用端口80作为MAMP Apache端口的缺点是始终会要求您输入密码。
最后，在“Web Server”选项卡上，您需要设置文档根目录。 这就是你所有的文件将用于你的本地网络服务器的地方。 文档根目录的例子是/Users/USERNAME/ Site /wordpress/。
编辑完所有设置后，点击OK保存。

3. 启动MAMP服务器并创建数据库:要启动MAMP Apache和MySQL服务器，只需点击主MAMP屏幕上的“Start Servers”即可。 你的MAMP服务器现在已经启动了。
一旦MAMP服务器启动，MAMP开始页面应该在您的默认Web浏览器中打开。 如果没有，点击MAMP窗口中的“Open start page”。 一旦打开，从网页选择phpMyAdmin。
在“Create new database”下，输入数据库名称，如“wordpress”，然后按“Create”。 无需为“collation”选择一个选项：在安装WordPress的过程中，当数据库表创建时，它将自动由MySQL分配。

4. 下载和安装WordPress
现在是[下载WordPress](https://wordpress.org/download/)的时候了。 下载并解压缩WordPress后，打开“wordpress”文件夹。 点击并拖动wordpress文件夹中的所有文件到你的MAMP文档根目录(/Users/USERNAME/Sites/wordpress/)。
其他的默认MAMP安装应该重命名并拖动文件夹到位于/Applications/MAMP下的htdocs文件夹。 然后在浏览器中，转到localhost:port/folder_renamed来运行安装。 例如，在默认的MAMP安装中，如果该文件夹被重命名为wordpresstest，请转到localhost:8888/ wordpresstest。
最后，我们必须运行[WordPress著名的5分钟安装](https://codex.wordpress.org/zh-cn:%E5%AE%89%E8%A3%85WordPress)。
访问本地站点（localhost:port或localhost:port/wordpress），然后在数据库设置表单中输入以下信息：
``` 
Database Name: wordpresstest
User Name (database): root
Password (database): root
Database Host/server: localhost
Table Prefix: wp_
```
请注意，默认的数据库名称是“Wordpress”，您需要将数据库名称更改为您输入到PHP管理员的名称（在本例中为“wordpresstest”）。 如果您的本地计算机上有多个WordPress站点，且每个站点都使用自己的数据库，则需要使WordPress配置中的数据库名称与您的第二个（或第三个或第四个）数据库名称保持一致。
完成后，输入博客名称和电子邮件地址，即可在Mac上使用WordPress。






