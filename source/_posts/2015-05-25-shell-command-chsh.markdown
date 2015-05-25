---
layout: post
title: "shell command - chsh"
date: 2015-05-25 23:28:15 +0800
comments: true
categories: 
---
更换系统当前shell，可以使用chsh命令。

1、查看当前系统安装的shell类型：cat /etc/shells

2、查看默认shell：echo $SHELL

3、切换shell：chsh -s /bin/zsh

4、查看当前shell的方法：

    a、echo $0

    b、echo $$，得到进程号；ps -ef | grep [进程号]
