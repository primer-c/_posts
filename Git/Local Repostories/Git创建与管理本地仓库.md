---
date: October 25 2020
title: Git创建与管理本地仓库
tags: Git
comments: true
---

#### 1.创建本地仓库

1. 创建工作区(Work Space)

   ```bash
   mkdir project & cd project
   ```

2. 初始化本地仓库()

   ```bash
   git init
   ```

3. 新建文件

   ```bash
   touch index.html
   ```

4. 查询状态

   ```bash
   git status
   ```

5. 将项目添加到暂存区

   ```bash
   git status
   ```

6. 将暂存区项目提交至本地仓库

   ```bash
   git commit -m "<message>"
   ```

#### 2.创建与管理分区

1. 查询分支

   ```bash
   git branch
   ```

2. 创建分支： dev

   ```bash
   git branch dev
   ```

3. 切换分支

   ```bash
   git checkout dev
   ```

4. 合并分支：主分支合并 dev 分支

   ```bash
   git checkout master
   git merge dev
   ```

#### 3.参考文当

[[Git 教程]](https://web-oyster.github.io/2020/10/25/Git/Tutorial/Git%E6%95%99%E7%A8%8B/)

#### 3. 联系方式

[[Email]](yuanmin8888@outlook.com)
