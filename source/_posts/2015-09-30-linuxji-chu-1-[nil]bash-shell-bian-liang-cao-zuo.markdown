---
layout: post
title: "linux基础(1)－bash shell 变量操作"
date: 2015-09-30 10:22:25 +0800
comments: true
categories: 
---
1、赋值：name=erika
   引申：不能在＝号左右有空格；如果要表示有空格的字符串，使用双引号或单引号：name="erika lxq"/'erika lxq';
   单引号和双引号的区别：单引号中的变量访问无效，双引号则可以转换出变量值：如name2='$name lxq'; name2="$name lxq"; 后者值为:erika lxq lxq;前者为字面值。

2、清空变量：unset [value]

3、在一串指令中调用另一串指令：version＝$(uname -r)

4、uname -r 为取系统核心版本号

5、变量拼接：PATH=${PATH}:/home/bin

6、将变量写入环境变量中：export value

7、额外说一句：直接输入cd就可以回到用户目录

8、RANDOM变量，大多数distributions都有该变量，用于生成随机数，范围在（0～32767）间，如果要在(0~9)之间，需要额外处理一下：declare -i number=$RANDOM*10/32768; echo $number;

9、PS1变量设置，该变量控制bash右侧输入符的格式，直接看例子：

［root@www home］# PS1='[\u@\h\w\A#\#\$]'

[root@www /home 17:00 #85]#

具体参数内容自行百度

9、$也是变量，表示当前进程pid，echo $$

10、?变量，代表上一个指令的回传值；echo $?


