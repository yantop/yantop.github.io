---
title: docker---PHP7容器添加memcache扩展
date: 2017-11-03 13:33:30
tags:
---
###大家好，欢迎来到我的github的博客站点！！！
####1.进入PHP容器
![这里写图片描述](http://img.blog.csdn.net/20171103132730120?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzY5NzkwMjQ=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
####2.下载PHP的memcache的扩展文件
> wget https://github.com/websupport-sk/pecl-memcache/archive/php7.zip
####3.解压扩展文件
> unzip php7.zip
####4.进入解压后的目录
> cd pecl-memcache-php7
####5.使用phpize安装扩展
![这里写图片描述](http://img.blog.csdn.net/20171103132842787?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzY5NzkwMjQ=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
####6.编译安装
![这里写图片描述](http://img.blog.csdn.net/20171103132903986?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzY5NzkwMjQ=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
#####7.查看memcache.so
![这里写图片描述](http://img.blog.csdn.net/20171103132932866?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzY5NzkwMjQ=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
####8.添加扩展文件，在docker-php-ext-memcache.ini中添加
> extension=memcache.ini   //保存退出
![这里写图片描述](http://img.blog.csdn.net/20171103133019327?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzY5NzkwMjQ=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
####9.查看phpinfo();
![这里写图片描述](http://img.blog.csdn.net/20171103133059472?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzY5NzkwMjQ=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
到此，php7的memcache扩展就顺利安装了。