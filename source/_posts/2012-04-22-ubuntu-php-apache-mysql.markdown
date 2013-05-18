---
layout: post
title: "Ubuntu搭建PHP+Apache+MySQL环境"
date: 2012-04-22 13:33
comments: true
categories: [Ubuntu, Web, PHP, Apache, MySQL]
---

安装Apache2

打开终端，输入“sudo apt-get install apache2”，回车;（安装apache2.0）
有密码输入密码，回车
输入“Y”，回车
apache2.0安装完成
验证apache2.0安装是否完成，在浏览器中打开http://localhost/或者http://127.0.0.1，出现It works!证明成功;

<!--more-->

安装PHP5

打开终端，输入“sudo apt-get install php5”，回车;（此为安装PHP）
输入“Y”，回车;
输入“sudo apt-get install libapache2-mod-php5”，回车;（此为配置APACHE+PHP）
输入“sudo /etc/init.d/apache2 restart”，回车;（此为重启APACHE）
输入“gksudo gedit /var/www/index.php”，回车;（此为测试PHP的安装结果）
然后输入
在浏览器中输入http://127.0.0.1/index.php或者http://localhost/index.php，出PHPINFO证明安装成功;
安装MySQL

在终端输入“sudo apt-get install mysql-server”，回车;（此为安装MYSQL）
输入“Y”，回车;
设置root密码;
在终端中输入“sudo apt-get install libapache2-mod-auth-mysql”，回车;（此为让apache、php支持 mysql）
在终端输入“sudo apt-get install php5-mysql”，回车;
在终端输入“sudo /etc/init.d/apache2 restart”，回车;
大功告成，继续折腾。
