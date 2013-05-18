---
layout: post
title: "Ubuntu Apache虚拟主机设置"
date: 2012-04-26 13:29
comments: true
categories: [VirtualHost, Apache, Ubuntu]
---

修改hosts是必须的，例如在本地测试我的博客，hosts文件中添加 127.0.0.1  demo.ifffff.com 


打开终端，cd /etc/apache2/sites-available 回车

sudo cp default demo.ifffff.com

sudo gedit demo.ifffff.com

<!--more-->

复制下面的文字到demo.ifffff.com这个文件中，ServerName和DocumentRoot改成你自己的。

<VirtualHost *:80>
ServerName demo.ifffff.com
ServerAdmin admin@ifffff.com
DocumentRoot “/var/www/ifffff/”
ErrorLog “/var/log/apache2/edunuke_errors.log”
CustomLog “/var/log/apache2/edunuke_accesses.log” common
</VirtualHost>

终端输入：
sudo a2ensite demo.iffff.com 回车

这样的话，虚拟主机站点 demo.ifffff.com 就已经安装好了。这时也可以在 /etc/apache2/sites-enabled/ 目录中发现多了一个到/etc/apache2/sites-available/demo.ifffff.com 的软链接。接下来就是将 Apache2 重启来使虚拟主机站点运行起来：

sudo /etc/init.d/apache2 restart 这里可以使用reload 重新加载

访问demo.ifffff.com 一切就妥妥的了～