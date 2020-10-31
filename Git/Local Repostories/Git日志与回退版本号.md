---
date: October 25 2020
title: Git日志与回退版本号
tags: Git
comments: true
---

#### 1.Git 日志

- 查看日志信息

  ```bash
  git log
  git log --pretty=oneline
  git reflog
  ```

- b:向回翻页

- 空格：向前翻页

#### 2.Git 版本控制

1. 版本回退

- 版本回退上一版本

  ```bash
  git reset --hard HEAD^
  git reset --hard HEAD~1
  ```

- 版本回退三步版本

  ```bash
  git reset --hard HEAD^^^
  git reset --hard HEAD~3
  ```

- 版本回退帮助查询

  ```bash
  git help reset
  ```

- `--soft参数`: 仅在本地库移动指针
- `--mixed参数`:
- `--hard参数`：

2. 删除版本找回

- 永久删除文件的找回操作

  ```bash
  git add <filename>
  # or
  git rm <filename>
  ```

- 添加到暂存区的删除文件找回

#### 3.比较文件差异

- 工作区与暂存区版本比较

  ```bash
  git diff <filename>
  ```

- 工作区文件与本地库历史记录比较

  ```bash
  git diff HEAD <filename>
  ```

- 工作区文件与本地库当前版本比较

  ```bash
  git diff HEAD
  ```

#### 4.参考文当

[[Git 教程]](https://web-oyster.github.io/2020/10/25/Git/Tutorial/Git%E6%95%99%E7%A8%8B/)

#### 3. 联系方式

[[Email]](yuanmin8888@outlook.com)
