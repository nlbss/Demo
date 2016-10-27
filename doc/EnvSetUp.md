# 搭建php服务器，访问、修改项目说明

### 一、KODExplorer

**1.KODExplorer是什么？**

KODExplorer(http://www.kalcaddle.com/index.html)是一个公开源码的基于Web的在线文件管理、代码编辑器。
它提供了类windows经典用户界面，一整套在线文件管理、文件预览、编辑、上传下载、在线解压缩、音乐播放功能。
让你直接在浏览器端实现web开发、源码文件预览、网站部署的同时拥有与本地操作一样方便、快捷、安全的体验。

**2.下载源码。**

 打开上面的连接，在其导航栏中的 "下载" 中将其源码(11M)下载下来。

### 二、php服务器的搭建

**1.下载集成软件包。**

在这里，我们使用的是 xampp，地址(http://rj.baidu.com/soft/detail/12489.html?ald)【普通下载就可】
或者打开  KODExplorer 的首页，点开导航栏的关于，单击右侧的安装步骤下序号 0              中的xampp。
   
**2.安装xampp。**

其安装路径尽量不要有中文。我就直接装在了D盘下的xampp文件夹中，安装完成后打开目录，
要注意"htdocs"文件夹，因为之后需要把项目放到这个文件夹里才可以访问到哦。
 
**3.配置xmapp。**

对于大多数人而言，因为曾经安装过SQLSERVER、MySQL或者Apache等软件，
导致端口的复用。因此在错误窗口常看到report的字样~~~这时候，需要修改端口。Apache的端口默认为80，
MySQL的端口默认为3306,同时需要注意，Apache配置的时候还需要配置一下SSL的端口，其默认端口443.
 为了避免端口冲突，我选择了修改apache的配置文件，将Apache的端口号改为8000
【点击Config-->Apache(httpd.confi)】， 打开后直接Ctrl+F，
  查找80，将80改为8000；因为之前我装过MySQL，配置MySQL的端口方法类似。

**4.访问Apache主页。**

在浏览器地址栏中输入http://localhost:8000/，
 如果出现了标题为"XAMPP Apache + MariaDB + PHP + Perl"的网页，说明成功了。
 如果无法访问该网站，啊哦，抱歉，第三步的配置有问题。

**5.在服务器上访问KODExplorer。**

将开始的第2步下载下来的目录名为KODExplorer的源码复制到上面提到的"htdocs"文件夹中，
因为"htdocs"文件加相当于前面输入的http://localhost:8000/，这是我测试了好一会才测出来的。
回车后就会访问到KODExplorer，之后就可以修改代码以及查看效果了。



