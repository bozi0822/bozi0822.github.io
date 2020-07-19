---
title: nginx启动报错解决方法
---
# [nginx启动报错：nginx: [error\] open() "/var/run/nginx/nginx.pid" failed (2: No such file or directory) 的解决办法](https://www.cnblogs.com/chenmingjun/p/10052205.html)



问题：

　　重启虚拟机后，再次重启nginx会报错： nginx: [error] open() "/var/run/nginx/nginx.pid" failed (2: No such file or directory) 

问题原因：

　　提示信息说明在 **/var/run/nginx/** 目录下找不到 **nginx.pid** 文件，解决方式有两种：

　　　　第一种方式：创建默认目录 **/var/run/nginx/** ；

　　　　第二种方式：修改 **nginx.conf** 文件，指定 **pid文件** 所在目录，我们演示第二种方式。如下：

解决方法：

　　（1）进入 **cd /usr/local/nginx/conf/** 目录，编辑配置文件**nginx.conf** ；

　　（2）在配置文件中有个注释的地方： **#pid        logs/nginx.pid;**

　　　　![img](https://img2018.cnblogs.com/blog/841693/201812/841693-20181202091211760-1232270726.png)

　　（3）将注释放开，并修改为：**pid    /usr/local/nginx/logs/nginx.pid;**

　　　　![img](https://img2018.cnblogs.com/blog/841693/201812/841693-20181202091241654-2034612437.png)

　　（4）在 **/usr/local/nginx** 目录下创建 **logs 目录**：**mkdir /usr/local/nginx/logs**

　　（5）再次启动nginx服务：**cd /usr/local/nginx/sbin/** 问题解决

　　　　**![img](https://img2018.cnblogs.com/blog/841693/201812/841693-20181202091529040-630051096.png)**

More info: [出自博客](https://www.cnblogs.com/chenmingjun/p/10052205.html)

