---
date: October 28 2020
tags: Node
title: Mongodb安装为32位windows服务
commits: true
---

#### 1. 创建安装目录

- 创建db目录：F:\mongodb\data\db

- 创建log目录: F:\mongodb\data\log\

#####  mongoDB/bin/目录

- 启动

  ```bash
  > mongod --dbpath F:\mongodb\data\db --storageEngine=mmapv1
  ```

#### 配置： 将MongoDB安装为windows服务

- 新建mongod.cfg文件，放在mongodb安装文件的bin目录下，内容如下：

  ```bash
  port=27017
  journal=true
  logappend=true
  storageEngine=mmapv1
  dbpath=F:\mongodb\data\db
  logpath=F:\mongodb\data\log\mongodb.log
  ```

- `管理员身份`打开cmd命令行，进入MongoDB安装目录的 bin目录：

```bash
bin>mongod --config "C:\mongodb\mongodb.config"  --install --serviceName "MongoDB"
```

如图结果存放在日志文件中，查看日志发现已经成功。如果失败有可能没有使用管理员身份，遭到拒绝访问

#### 启动mongodb服务 

- 启动windows服务

- 打开cmd输入`services.msc`，点击启动,查看服务可以看到MongoDB服务;


#### 3.参考文档

[[1. MongoDB教程]](https://web-oyster.github.io/2020/10/28/DataBase/MongoDB/Tutorial/MongoDB%E6%95%99%E7%A8%8B/)

#### 4. 联系方式

[[Email]](yuanmin8888@outlook.com)