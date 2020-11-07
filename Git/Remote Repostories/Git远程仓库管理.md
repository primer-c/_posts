---
date: October 25 2020
title: Git远程仓库管理
tags: Git
comments: true
---

#### 1. Github SSH 仓库地址

- 地址组成

  ```bash
  git@github.com:web-oyster/html-elements.git
  ```

- git@github.com： git 网址
- web-oyster： github 账号
- html-elements： github 远程仓库名

#### 2. 创建远程仓库关联

- git 初始化本地仓库

  ```bash
  git init
  ```

- 创建远程仓库

[[快速创建 Github 远程仓库]](https://web-oyster.github.io/2020/10/25/Git/Remote%20Repostories/%E5%BF%AB%E9%80%9F%E5%88%9B%E5%BB%BAGithub%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93/)

- 第一次提交：关联远程仓库地址

  ```bash
  git remote add origin git@github.com:<github账号>/<github远程仓库名>.git
  git pull
  ```

- 第二次提交

  ```bash
  git push
  ```

- 参考文档

[[快速创建 Github 远程仓库]](https://web-oyster.github.io/2020/10/25/Git/Remote%20Repostories/%E5%BF%AB%E9%80%9F%E5%88%9B%E5%BB%BAGithub%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93/)

#### 3. 参考文档

[[Git 教程]](https://web-oyster.github.io/2020/10/25/Git/Tutorial/Git%E6%95%99%E7%A8%8B/)

#### 4. 联系方式

[[Email]](yuanmin8888@outlook.com)
