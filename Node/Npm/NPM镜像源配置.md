---
date: October 24 2020
title: 3.NPM镜像源配置
tags: Node
comments: true
---

#### 1. 单次使用

- command line 配置

  ```bash
  npm install --registry=https://registry.npm.taobao.org
  ```

#### 2. 永久使用

1. 设置成全局下载镜像站点，每次安装软件默认从淘宝镜像下载：

2. 方法一

- 打开.npmrc 文件： `nodejs\node_modules\npm\npmrc`
- 没有的话可以使用 git 命令行新建：

  ```bash
  touch .npmrc
  ```

- 增加一行: `registry =https://registry.npm.taobao.org` 即可；

3. 方法二

- 命令行设置

  ```bash
  npm config set registry https://registry.npm.taobao.org
  ```

- 测试

  ```bash
  npm config get registry    // 或
  npm info express    //输出：https://registry.npm.taobao.org/  ok
  ```

#### 3. 参考文档

[[NPM 包管理器]](https://web-oyster.github.io/2020/10/24/Node/Npm/NPM%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8/)

#### 4. 联系方式

[[Email]](yuanmin8888@outlook.com)
