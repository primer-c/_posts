---
date: October 28 2020
tags: Ubuntu
title: 1. Ubuntu20.04系统安装
comments: true
---

#### 1. 下载

1. 下载 Ubuntu20.04

- [[下载地址：]](https://ubuntu.com/download/desktop)

2. 下载 Rufus

- [[下载地址：]](http://rufus.ie/)

#### 2. 制作 Rufus 启动盘

- windows 系统，双击 rufus， =>SELECT =>Ubuntu20.04 ISO 文件=>Start

  ![[rufus]](https://s1.ax1x.com/2020/10/02/0QGOOI.png)

#### 3. 安装 Ubuntu

1. 配置系统启动

以 Acer 为例:

- 开机 => F2 =>F6
- 将 USB 启动盘提升到顶部=>F10=>Yes
- 重启系统自动安装

#### 4. wifi 设置

- 点击右上角下三角形，根据提示选择无线网络，设置 wifi 密码

#### 5. 国内镜像源配置

- 获取文件编辑权限

  ```bash
  sudo chmod 777 /etc/apt/sources.list
  gedit /etc/apt/sources.list
  ```

- 复制粘贴镜像源

  ```bash
  #tsinghua mirrors

  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse

  # aliyun mirrors

  deb http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse
  ```

#### 6. 系统更新

- 更新

  ```bash
  sudo apt-get update
  sudo apt-get upgrade
  ```

#### 7. 参考文档

[[2.Ubuntu 系统及应用软件安装与配置]](https://web-oyster.github.io/2020/10/24/Linux/Ubuntu/Ubuntu%E7%B3%BB%E7%BB%9F%E5%8F%8A%E5%BA%94%E7%94%A8%E8%BD%AF%E4%BB%B6%E5%AE%89%E8%A3%85%E4%B8%8E%E9%85%8D%E7%BD%AE/)

#### 8. 联系方式

[[Email]](yuanmin8888@outlook.com)
