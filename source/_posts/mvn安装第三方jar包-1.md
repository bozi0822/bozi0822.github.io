---
title: mvn安装第三方jar包
date: 2020-08-12 19:37:23
tags: JAVA WEB
---



### 安装第三方jar包到本地仓库

##### ----进入jar包所在目录运行

```
mvn install:install-file -DgroupId=com.alibaba -DartifactId=fastjson -Dversion=1.1.37 -Dfile=fastjson-1.1.37.jar -Dpackaging=jar
```

##### ----打开cmd直接运行

```
mvn install:install-file -DgroupId=com.alibaba -DartifactId=fastjson -Dversion=1.1.37 -Dpackaging=jar -Dfile=C:\my_java\授课资料\资料：maven【高级】\安装第三方jar包\fastjson-1.1.37.jar
```


##### --安装第三方jar包到私服

##### --在settings配置文件中添加登录私服第三方登录信息

```
<server>
  <id>thirdparty</id>
  <username>admin</username>
  <password>admin123</password>
</server>
```

##### 进入jar包所在目录运行

```
mvn deploy:deploy-file -DgroupId=com.alibaba -DartifactId=fastjson -Dversion=1.1.37 -Dpackaging=jar -Dfile=fastjson-1.1.37.jar -Durl=http://localhost:8081/nexus/content/repositories/thirdparty/ -DrepositoryId=thirdparty
```

##### 打开cmd直接运行

```
mvn deploy:deploy-file -DgroupId=com.alibaba -DartifactId=fastjson -Dversion=1.1.37 -Dpackaging=jar -Dfile=C:\my_java\授课资料\资料：maven【高级】\安装第三方jar包\fastjson-1.1.37.jar -Durl=http://localhost:8081/nexus/content/repositories/thirdparty/ -DrepositoryId=thirdparty
```

