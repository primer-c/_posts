---
date: October 24 2020
title: 2.Windows安装与配置Nvm
tags: Node
comments: true
---
#### 1. 下载

[[下载地址]](https://github.com/coreybutler/nvm-windows/releases)

- 下载版本： `nvm-noinstall.zip`

- 解压

#### 2. 安装

- 安装目录： `F:/Application/Nvm/nvm`

  ![[安装目录]](https://s1.ax1x.com/2020/10/15/0TAl59.png)

- 创建目录`node`存放Node依赖包: `F:/Application/Nvm/node`

- 打开nvm目录，点击`install.exe`文件，生成settings.text文件

  ![[安装nvm]](https://s1.ax1x.com/2020/10/15/0TAtKK.png)

- 转贴安装目录和Node依赖包目录，如下图：

  ![[配置文件]](https://s1.ax1x.com/2020/10/15/0TERQx.png)

#### 3. 配置NPM环境变量

- npm 配置镜像源: settings文件配置

  ```bash
  node_mirror: https://npm.taobao.org/mirrors/node/
  npm_mirror: https://npm.taobao.org/mirrors/npm/
  ```

- 配置图

  ![[Nvm配置图]](https://s1.ax1x.com/2020/10/27/BMA8Rs.jpg)

#### 4. 使用

1. 安装不同版本 Node

- 查看node版本号

  ```bash
  nvm list
  ```

- 安装指定版本

  ```bash
  nvm install node <version>
  ```
- 查看安装node不同版本

  ![[使用]](https://s1.ax1x.com/2020/10/15/0TAVg0.png)

- 使用特定版本的node

  ```bash
  nvm use 12.0.0
  ```

- 测试node使用版本

  ```bash
  node -v
  ```

#### 5. 参考文档

[[NPM 包管理器]](https://web-oyster.github.io/2020/10/24/Node/Npm/NPM%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8/)

#### 6. 联系方式

[[Email]](yuanmin8888@outlook.com)
