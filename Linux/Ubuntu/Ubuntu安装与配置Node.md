---
date: October 24 2020
title: 1.Ubuntu20.04 安装与配置Node
tags: Ubuntu
comments: true
---

#### 1. 安装

- 系统追加 PPA

  ```bash
  sudo apt install curl
  curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
  ```

- 安装开发工具

  ```bash
  sudo apt-get install gcc g++ make
  ```

- 安装 Node

  ```bash
  sudo apt-get install nodejs
  ```

- 测试安装版本: 关闭终端，重启终端

  ```bash
  node -v
  npm -v
  ```

#### 2. 修改镜像源

```bash
npm config set registry https://registry.npm.taobao.org\
```

- 测试

  ```bash
  npm info underscore
  ```

- npm 配置镜像源

  ![npm配置镜像源](https://s1.ax1x.com/2020/10/24/BZCbT0.png)

- 参考文档

[[NPM 镜像源配置]](https://web-oyster.github.io/2020/10/24/Node/Npm/NPM%E9%95%9C%E5%83%8F%E6%BA%90%E9%85%8D%E7%BD%AE/)

#### 5. 参考文档

[[2.Ubuntu 系统及应用软件安装与配置]](https://web-oyster.github.io/2020/10/24/Linux/Ubuntu/Ubuntu%E7%B3%BB%E7%BB%9F%E5%8F%8A%E5%BA%94%E7%94%A8%E8%BD%AF%E4%BB%B6%E5%AE%89%E8%A3%85%E4%B8%8E%E9%85%8D%E7%BD%AE/)

[[NPM 包管理器]](https://web-oyster.github.io/2020/10/24/Node/Npm/NPM%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8/)

#### 6. 联系方式

[[Email]](yuanmin8888@outlook.com)
