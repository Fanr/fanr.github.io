---
layout: post
title: "解决Win8 IE10无法打开"
date: 2013-01-11 12:25
comments: true
categories: [Windows, IE10]
---

装了一堆常用(根本不用)软件,不知道是哪个,直接导致IE10无法打开,但却可以使用管理员权限打开.

卸载重新安装,未果.

<!--more-->

唯一解决方案

WIN+R, 输入regedit,回车

找到 HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\Main

右键Main,选择权限.

高级，右下角的“启用继承”按钮即可。

目测只能编辑注册表修正