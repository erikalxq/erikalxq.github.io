---
layout: post
title: "hadoop install on MacOSX"
date: 2015-09-17 14:19:48 +0800
comments: true
categories: 
---

hadoop版本下载的是最新的2.7.1，支持jdk7+，不再支持jdk6+ 
http://hadoop.apache.org/releases.html#06+July%2C+2015%3A+Release+2.7.1+%28stable%29+available

jdk下载的是最新的jdk8u60版本
http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html

默认的mac自带jdk路径为：/System/Library/Frameworks/JavaVM.framework/Versions

安装的jdk路径在：/Library/Java/JavaVirtualMachines/jdk1.8.0 60.jdk/Contents/Home

所以需要将环境变量修改：

export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0 60.jdk/Contents/Home

同时解压hadoop，修改环境变量：

export HADOOP_INSTALL=压缩包路径; 
export PATH=$PATH:$HADOOP_INSTALL/bin

重启终端，输入hadoop version，应该就可以看到hadoop的版本号了;

我使用的是zsh终端，所以修改的是～/.zshrc文件的环境变量
