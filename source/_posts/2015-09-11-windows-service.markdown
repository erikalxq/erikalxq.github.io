---
layout: post
title: "windows service"
date: 2015-09-11 14:08:15 +0800
comments: true
categories: 
---
对于用vc＋＋写的windows服务，使用installutil来安装服务会出现一些问题：__clrcall，工程属性为pure /clr，改为/clr后部署失败；但不修改这个属性的话，在使用线程函数又会报错：__clrcall、__stddll无法确认；

所以换成sc create 方式来安装服务；

安装服务：
sc create serviceName binpath= "fullpath"

删除服务：
需要先退出服务管理器，否则会出现服务已被标记为删除的情况
sc delete serviceName

sc start serviceName

sc stop serviceName
