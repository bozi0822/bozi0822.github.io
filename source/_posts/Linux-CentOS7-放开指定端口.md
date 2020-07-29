Linux-CentOS7-放开指定端口

执意丨 2019-04-17 14:30:44  1564  收藏 2
分类专栏： CentOS7 Linux
版权
我这里以80端口为例（在防火墙开启的情况下才存在）
放开端口(如下表示成功)
我这里以80端口为例（在防火墙开启的情况下才存在，防火墙关闭的话所有端口都可以访问）

[root@os-one ~]# firewall-cmd --zone=public --add-port=80/tcp --permanent
success
[root@os-one ~]# 

关闭端口命令(如下表示成功)
[root@os-one ~]# firewall-cmd --zone=public --remove-port=80/tcp --permanent
success
[root@os-one ~]# 