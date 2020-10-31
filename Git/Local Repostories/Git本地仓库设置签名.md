---
date: October 25 2020
title: Git本地仓库设置签名
tags: Git
comments: true
---

#### 1.Git 本地仓库签名的作用

- 区分不同开发人员的身份和权限

#### 2.Git 地仓库签名与 Github 账号的关系

- 本地仓库签名与 Github 远程仓库登陆账号、密码没有任何关系

#### 3.签名格式

- user.name: 任意姓名就可
- user.email: 任意邮箱地址就可

#### 4.设置签名

- 项目(仓库)级别签名

  ```bash
  git config user.name andy
  git config user.email andy@gmail.com
  ```

- 系统级别签名

  ```bash
  git config --global user.name andy
  git config --global user.email andy@gmail.com
  ```

- 签名优先级别： 项目(仓库)级别签名优先于系统级别签名

- 查看项目签名

  ```bash
  cat .git/config
  ```

  ![[查看项目签名]](https://s1.ax1x.com/2020/10/30/BYTfRP.png)

- 查看系统签名

  ```bash
  cat ～/.gitconfig
  ```

  ![[查看系统签名]](https://s1.ax1x.com/2020/10/30/BYTVbQ.png)

#### 3. 参考文档

[[Git 教程]](https://web-oyster.github.io/2020/10/25/Git/Tutorial/Git%E6%95%99%E7%A8%8B/)

#### 4. 联系方式

[[Email]](yuanmin8888@outlook.com)
