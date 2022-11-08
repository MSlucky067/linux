MySQL的安装与配置——详细教程

⭐Published on 2019-09-15 20:13 in 分类: [数据库](https://www.cnblogs.com/winton-nfs/category/1543851.html) with [Winton-H](https://cnblogs.com/winton-nfs) 🎈🎈🎈
⭐一个人其实也挺好，没有惊喜，没有期盼，没有吃醋，没有失望，也没有辜负，你说是吧？🍃
⭐自律，才是自己所拥有的最好的资本🍃
⭐到后来才慢慢懂得，或许戳破那层窗纸，没有比埋藏在心里好，这也许就是很多人长大之后渐渐很多事都不愿随意吐露的原因吧

分类: [数据库](https://www.cnblogs.com/winton-nfs/category/1543851.html)

# 

# 　免安装版的Mysql

　　MySQL关是一种关系数据库管理系统，所使用的 SQL 语言是用于访问[数据库](https://baike.baidu.com/item/数据库/103728)的最常用的

标准化语言，其特点为体积小、速度快、总体拥有成本低，尤其是[开放源码](https://baike.baidu.com/item/开放源码/7176422)这一特点，在 Web

应用方面 MySQL 是最好的 RDBMS(Relational Database Management System：关系数据

库管理系统)应用软件之一。

 

　　在本博文里，我主要以Mysql免安装版为例，帮助大家解决安装与配置mysql的步骤。

 

　　首先：要先进入mysql官网里（Mysql的官网-->https://www.mysql.com/），下面是详细步骤：↓

　　(为了方便大家的操作，我的网盘里有安装包：

　　　　链接：https://pan.baidu.com/s/1hq0rrtdXm2g7FqwaBKxgWg
　　　　提取码：wsh6
　　)

 

 



## **一、下载安装包：**

　　①进入官网后，点击"Dowload"，然后页面往下拉

　　**![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915192559647-350219166.jpg)**

　　

 

　　②接下来看到的页面是这样的，红色框框的链接就是mysql社区版，是免费的mysql版本，然后我们点击这个框框的链接：↓

 

　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915192752591-1371678378.jpg)

 

 

　　　 ③接下来跳转到这个页面，在这里，我们只要下载社区版的Server就可以了：↓

![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915193055444-1634354218.jpg)

 

 

　　④下载免安装版(windows以外的其他系统除外)

 

![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915193247068-1867170933.jpg)

 

　　 ***这样，安装包就下载好了！

　　***注意，安装的目录应当放在指定位置，，其次，绝对路径中避免出现中文，推荐首选英文为命名条件！！！！(我的为参考)

　　

　　**![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915193949895-2127429091.jpg)**

 

 



## **二、Mysql的配置**

　　***以管理员身份打开命令行(如下图所示)，一定要是管理员身份，否则由于后续部分命令需要权限，出现错误！**

　　**![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915194138600-1666145922.jpg)**

　　

　　①下转到mysql的bin目录下：**
**

 

　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915194319422-1269147823.jpg)

 

　　②安装mysql的服务：mysqld --install

 

　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915194355509-621408710.jpg)

　　

 

　　③初始化mysql，在这里，初始化会产生一个随机密码,如下图框框所示，记住这个密码，后面会用到(mysqld --initialize --console)

　　

　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915194537624-1288770126.jpg)

　　

　　④开启mysql的服务(net start mysql)

 

　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915194809019-447378790.jpg)

 

 

　　⑤登录验证，mysql是否安装成功！(要注意上面产生的随机密码，不包括前面符号前面的空格，否则会登陆失败)，如果和下图所示一样，则说明你的mysql已经安装成功！注意，，一定要先开启服务，不然会登陆失败，出现拒绝访问的提示符！！！

 

　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915194855594-1799062186.jpg)

 

 

　　**修改密码：**

　　　　由于初始化产生的随机密码太复杂，，不便于我们登录mysql，因此，我们应当修改一个自己能记住的密码！！

 

　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915195232011-1164270181.jpg)

 

 

　　再次登录验证新密码：

 

　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915195310138-1959548424.jpg)

 

 

　　**设置系统的全局变量：**

　　　　为了方便登录操作mysql，在这里我们设置一个全局变量：↓

 

　　　　①点击"我的电脑"-->"属性"-->''高级系统设置''-->''环境变量'',接下来如下图所操作

　　

　　　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915195658938-215279743.jpg)

 

 

　　　　②把新建的mysql变量添加到Path路径变量中，点击确定，即完成：

 

　　　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915195808186-1920486822.jpg)

 

　　　　

　　　　配置完成之后，每当我们想要用命令行使用mysql时，只需要win+R，-->输入"cmd"打开命令行，之后输入登录sql语句即可。

 

　　

　　　　③在mysql目录下创建一个ini或cnf配置文件，在这里我创建的是ini配置文件，里面写的代码是mysql的一些基本配置

 

　　　　![img](https://img2018.cnblogs.com/blog/1727568/201909/1727568-20190915201058332-997469892.jpg)

 

 

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
[mysqld]
character-set-server=utf8mb4
bind-address=0.0.0.0
port=3306
default-storage-engine=INNODB
[mysql]
default-character-set=utf8mb4
[client]
default-character-set=utf8mb4
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

 

 

　　就这样，一个免安装版的Mysql就安装并配置完成了

 

 



### 2.1可能会出现的问题

 1、ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: NO/YES) 

 2、"由于找不到MSVCR120.dll，无法继续执行代码。重新安装程序可能会解决此问题" 或者 "由于找不到VCRUNTIME140_1.dll，无法继续执行代码。重新安装程序可能会解决此问题" 

 3、"net start Mysql"启动服务时 ，显示"Mysql服务正在启动  Mysql服务无法启动  服务没有报告任何错误"

 

**解决办法**： 转移至我另外两篇博客

1、[ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: NO/YES)](https://www.cnblogs.com/winton-nfs/p/12956811.html) 

2、[解决mysql问题：由于找不到MSVCR120.dll,无法继续执行代码.重新安装程序可能会解决此问题。](https://www.cnblogs.com/winton-nfs/p/13854052.html) 

3、待续，正在撰写相关博客，如遇到此问题，可评论，博主回复解决

 

 

 



### 2.2命令参考：

 

　　**①安装服务：**mysqld --install

 

　　**②\**初始化：\****　mysqld --initialize --console

 

　　***\*③开启服务：\****net start mysql

 

　　***\*④关闭\*\*\*\*服务：\*\*\*\*\****net stop mysql

 

　　***\**\*\*\*⑤登录mysql：\*\*\*\*\****mysql -u root -p

 

　　　　***\**\*\*\*Enter PassWord：(\*\*\*\*\****密码***\**\*\*\*)\*\*\*\*\****

 

　　***\**\*\*\*⑥修改密码：\*\*\*\*\****alter user 'root'@'localhost' identified by 'root';(by 接着的是密码)

 

　　**⑦标记删除mysql服务**：sc delete mysql

 

　　

**文章可自行全篇转载或部分摘取，注明出处→贴个原文链接意思意思一下即可**

 