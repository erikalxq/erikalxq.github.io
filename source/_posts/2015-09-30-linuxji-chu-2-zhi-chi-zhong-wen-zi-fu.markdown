---
layout: post
title: "linux基础(2)-支持中文字符"
date: 2015-09-30 15:35:20 +0800
comments: true
categories: 
---
添加中文字符集
vim /var/lib/locales/supported.d/local
添加如下内容：
zh_CN.UTF-8 UTF-8
zh_CN.GBK GBK
zh_CN GB2312
保存后，执行命令：
sudo locale-gen

打开/etc/environment
在下面添加如下两行
LANG=”zh_CN.UTF-8″
LANGUAGE=”zh_CN:zh:en_US:en”

打开/etc/default/locale
修改为：
LANG=”zh_CN.UTF-8″
LANGUAGE=”zh_CN:zh:en_US:en”

重启
