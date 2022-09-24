# README

*本次项目一共用到了4个Jar类型的文件，分别是：activation,jar；flatlaf-2.4.jar；mail.jar；sqlite-jdbc-3.7.2.jar。从而实现发送邮件、数据库存取、UI优化的功能*

*以下是说明规范*

## 发送邮件

首先需要在机器上安装JavaMail API 和Java Activation Framework，下载链接如下：[](https://www.oracle.com/java/technologies/downloads.html)

**注意**

发送邮件的功能不能直接使用，为了保护隐私，我们选择将发送邮件的邮箱抹去，并将验证码进行抹去。为了您正常使用，以QQ邮箱为例，接下来讲述如何使用邮箱发送:

在QQ邮箱的设置页面，将POP3/SMTP服务打开：

并获取授权码：

然后再*RegisterUI*类中，找到*sendMail*方法：


再*sendEmai*l中输入您的邮箱，再*sendEmailPwd*中输入您的授权码，即可正常使用

## 数据库存取

sqlite3的下载链接为：[](https://www.sqlite.org/download.html)，如果使用的是*Windows*系统，则选择下载 *sqlite-tools-win32-\*.zip* 和 *sqlite-dll-win32-\*.zip* 压缩文件；然后创建文件夹 *C:\sqlite*，并在此文件夹下解压上面两个压缩文件，将得到 *sqlite3.def*、*sqlite3.dll* 和*sqlite3.exe* 文件；添加 *C:\sqlite* 到 PATH 环境变量，最后在命令提示符下，使用 **sqlite3** 命令，将显示如下结果：

```
C:\>sqlite3
SQLite version 3.7.15.2 2013-01-09 11:53:05
Enter ".help" for instructions
Enter SQL statements terminated with a ";"
sqlite>
```

### 数据库在项目中的具体使用

本次项目中一共存有两张表*Users*和*Maths*，所以您在使用之前需要先创建出这两个表，项目中提供了创建这两个表的方法

在*DatabaseOperation*类中，调用方法*createUsersTable*和*createMathsTable*实现表的创建

**第一次使用该软件时，必须先创建这两个表**

## UI优化

本项目通过使用*flatlaf*实现对界面的优化，*flatlaf*的下载链接：[](https://search.maven.org/artifact/com.formdev/flatlaf/2.4/jar),点击最右边的*Download*按钮进行下载


