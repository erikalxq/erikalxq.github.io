---
layout: post
title: "ubuntu+mysql远程访问"
date: 2015-09-30 17:31:23 +0800
comments: true
categories: 
---
1、修改可访问的用户信息：
mysql -uroot -p
use mysql;
GRANT ALL PRIVILEGES ON *.* TO "username" IDENTIFIED BY 'password' WITH GRANT OPTION;
flush privileges;

2、修改 /etc/mysql/my.cnf
//找到如下内容，并注释
bind-address = 127.0.0.1

注释掉 bind-address = 127.0.0.1 后重启mysql即可！如果不注释掉，通过netstat可以查看到，306端口只是在IP 127.0.0.1上监听，所以拒绝了其他IP的访问

3、可能防火墙问题
