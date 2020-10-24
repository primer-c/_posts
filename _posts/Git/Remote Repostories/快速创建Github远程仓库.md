---
date: October 25 2020
tags: 快速创建Github远程仓库
comments: true
---

#### 1. Github 服务器注册账号

- 注册用户名

#### 2. 创建远程仓库

- 方法一：左边栏 `Repositories`新建仓库

- 方法二：右上角 `+`新建仓库

- 创建仓库示意图

  ![创建仓库示意图](https://s1.ax1x.com/2020/10/25/BeuSED.png)

#### 3. 创建本地库

- 方法一： 克隆远程仓库

  ```bash
  git clone git@github.com:github_account/repository.git
  ```

- 克隆示意图

  ![克隆](https://s1.ax1x.com/2020/10/25/BenxHO.png)

- 方法二： 直接创建本地库

#### 4. 建立本地仓库与远程仓库关联

1.  创建公钥

- git 通过如下命令：

  1. 生成`.ssh`目录;
  2. 创建一对密钥： `id_rsa`(私钥)和`id_rsa.pub`(公钥)
  3. 其中 windows 系统在： C：盘的`administration`目录
  4. Ubuntu 系统存放在`Home`目录
  5. 编辑器打开公钥，将其复制到 Github 的`SSH and GPG keys`

  ```bash
  ssh-keygen -t rsa -C <Github注册邮箱>
  ```

- 测试

  ```bash
  ssh -T git@github.com
  ```

- 参考文档: [[Git 远程仓库管理]](https://yuanmin650304.github.io/2020/10/01/Git/Git%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93%E7%AE%A1%E7%90%86/)

#### 5. Git 拉取与推送文件

- 详见参考文档： [[Git 远程仓库管理]](https://yuanmin650304.github.io/2020/10/01/Git/Git%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93%E7%AE%A1%E7%90%86/)

#### 6. Git 命令

##### 1. create a new repository on the command line

- git init
- git add README.md
- git commit -m "first commit"
- git branch -M main
- git remote add origin git@github.com:web-oyster/blog_for_web-master.git
- git push -u origin main

##### 2. push an existing repository from the command line

- git remote add origin git@github.com:web-oyster/blog_for_web-master.git
- git branch -M main
- git push -u origin main

#### 7. 参考文档

[[Git]]()
