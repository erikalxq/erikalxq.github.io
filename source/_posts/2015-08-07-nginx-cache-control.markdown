---
layout: post
title: "nginx cache-control"
date: 2015-08-07 12:28:49 +0800
comments: true
categories: 
---
nginx服务器配置网站各类资源的缓存

使用的模块为nginx_http_headers_module

其实就是在nginx的配置文件内，可以在http/sever／location这些模块下添加不同类型站点文件的缓存有效时间，配置值为：expires

实例：

如设置某文件夹内文件的缓存有效值：
location ~ ^/image/{

	root /[image所在路径];
	
	expires 1h;	# m分钟\h小时\d天(也可以使用add_header Cache-Control 30d)

}

关于http缓存的参考知识：http://www.cnblogs.com/futan/archive/2013/04/21/cachehuancun.html

