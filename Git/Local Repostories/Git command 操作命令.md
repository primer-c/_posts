---
date: October 25 2020
title: Git command 操作命令
tags: Git
comments: true
---

#### 1.初始化操作命令

- 初始化操作

  ```bash
  git init
  ```

#### 2.查看资源操作命令

- 查看资源

  ```bash
  ll
  ```

- 查看隐藏资源

  ```bash
  ls -al
  ```

- 分屏查看资源

  ```bash
  ll | less
  ls -l | less
  ```

- 查看 git 本地仓库的子目录和文件

```bash
 ll .git/
```

#### 3. Git 设置签名

- Git 设置系统签名

```bash
 git config --global user.name andy
 git config --global user.email andy@gmail.com
```

- Git 设置项目签名

  ```bash
  git config user.name andy
  git config user.email andy@gmail.com
  ```

#### 4. Git 删除更改退回到修改前的状态

```bash
 git rm --cached <filename>
```

#### 3. 参考文档

[[Git 教程]](https://web-oyster.github.io/2020/10/25/Git/Tutorial/Git%E6%95%99%E7%A8%8B/)

#### 4. 联系方式

[[Email]](yuanmin8888@outlook.com)
