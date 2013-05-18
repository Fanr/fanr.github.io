---
layout: post
title: "清除MAC回收站中的顽固垃圾"
date: 2013-04-23 10:17
comments: true
categories: Mac
---

总是会遇到一些无法从回收站移除的文件，要么是单个文件，要么文件夹无限循环下去。

见不得回收站堆满垃圾，和不停的躲避贱人的追赶一样，眼不见心不烦。

<!--more-->

sudo -s

cd .Trash

rm -rf *

exit

搞定，收工。