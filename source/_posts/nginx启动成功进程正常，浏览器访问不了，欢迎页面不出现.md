---
title: nginx启动成功进程正常，浏览器访问不了
date: 2020-07-19 15:54:29
updated: 2020-07-20 15:47:27
categories: 
- Server
tags:
- JAVA WEB
---

nginx启动成功进程正常，浏览器访问不了，欢迎页面不出现

版权
自己搭建了nginx+tomcat 部署到服务器上面。 装好nginx，为了避免冲突，把其他进程都检查了一遍，没有占用80端口，所以默认使用80端口，安装好后，启动nginx，ps -ef | grep nginx 进程正常 使用浏览器访问时发现访问不了！
现在我分享一下我的解决方法，

1、先查看nginx配置是否正确
执行下面的命令:

	 nginx -t   #查看nginx配置是否正确  也可以切换到nginx的安装目录下的sbin目录下，执行: ./nginx -t
1
2、查看nginx是否启动成功

	ps -ef | grep nginx  #查看nginx端口
1
执行步骤1,2,后发现nginx配置没问题，且启动成功了！进程正常，我猜测是端口没开放。
3、.检查服务器对应的端口是否放开

查看端口是否开放

	telnet + ip + port  #如: telnet 192.168.157.129 80  
	#没有telnet命令使用：yum install telnet 安装后使用。
1
2
输入命令后得到如下，证明端口没有开放



(1)查看开放的所有端口
命令一

	netstat -a # 查看所有服务端口 
1
命令二

	nmap + ip地址 # 如：nmap 127.0.0.1
1
(2)很多时候 telnet 完就无法退出了，ctrl+c 有时也无法退出;
这个时候先执行：ctrl+] 然后在telnet 命令行输入 quit 就可以退出了
