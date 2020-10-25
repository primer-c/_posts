---
date: October 21 2020
title: Hexo创建博客
tags: Hexo
comment: true
---

#### 1. 安装 hexo 脚手架

- 全局安装 Hexo: 开启 Git

  ```bash
  $ sudo npm install -g hexo-cli
  ```

#### 2. 初始化项目

- 初始化 hexo

  ```bash
  $ cd hexo_blog
  $ hexo init
  $ git init
  ```

3. 本地部署

- Hexo 本地部署并测试

  ```bash
  $ hexo server
  ```

- localhost:4000

3. 安装插件

- 安装 ：hexo-deployer-git

  ```bash
  npm install hexo-deployer-git --save
  ```

4. 生成静态文件

- 生成目录和静态文件

  ```bash
  $ hexo generate
  $ hexo -g       //简写
  ```

5. 创建 github 仓库

- username: full-stoke
- repository: full-stoke-github.io

6. 修改配置文件

- \_config.yml

  ```yml
  deploy:
  type: git
  repo: git@github.com:full-stoke/full-stoke.github.io.git
  ```

7. 配置用户名和邮箱

- 项目配置

  ```bash
   $git config user.name "full-stoke"
   $git config user.email "username@gmai.com"
  ```

- 全局配置
  ```bash
  $git config --global user.name "full-stoke"
  $git config --global user.email "username@gmai.com"
  ```

8. 创建和配置公钥

- 创建 github 仓库：

  - [[网址：]](https://github.com)
  - 注册账号 ： <用户名>
  - 创建远程仓库： <用户名>github.io

- 本地仓库与 github 远程仓库关联时，需要在 github 配置公钥

- 创建 Github SSH key 密钥
- 创建一个 SSH key,在命令行（即 Git Bash）输入以下命令， 回车三下即可：
  ```bash
  $ ssh-keygen -t rsa -C "username@gmail.com"
  ```
- 生成：id_rsa(私钥) 和 id_rsa.pub(公钥),

- 打开公钥： id_rsa.pub
  ```bash
  cd ~/.ssh
  ```
- 编辑器打开 id_rsa.pub

- 复制公钥黏贴到 Github： SSH Key

- 测试是否添加成功

  ```bash
  $ ssh -T git@github.com
  ```

- 提示符下： 返回`“You’ve successfully authenticated”`即成功

#### 3. 部署

- deploy
  ```bash
  $ hexo deploy
  $ hexo clean
  $ hexo d -g #生成并上传
  ```

#### 4.故障处理

- 故障处理
  ```bash
  $ hexo clean	## 删除public目录，然后再来重新生成和发布
  ```

#### 5.配置文件范本

1. 配置文件：`\_config.yml`说明

   ```bash
   title: Hexo #站点的标题
   subtitle: #站点的副标题
   description: #站点的描述，写一段话来介绍你的博客吧:)，主要为SEO使用
   author: John Doe #显示的文章作者名字，例如我配置的是fourstring
   language: #语言。简体中文是zh-Hans
   timezone: #时区，可以不配置，默认以本地时区为准
   url: http://yoursite.com #你的站点地址，如果是全站HTTPS记得写成https://domain.com
   root: / #如果您的网站存放在子目录中，例如 http://yoursite.com/blog，则请将您的 url 设为 http://yoursite.com/blog 并把 root 设为 /blog/。（引用自官方文档）
   permalink: :year/:month/:day/:title/ #固定链接格式。这项配置的格式为：变量1/变量2/变量3...，其中合法的变量格式为“:变量名”（注意，:是变量的组成部分！）这样生成的效果为/2016/08/10/文章标题。默认的固定链接格式存在一些问题，下文讲解
   per_page: 10 #设置每页文章篇数，设为0可以关闭分页功能
   theme: #使用的主题。下文讲解
   type: git
   #部署配置，其值是一个杂凑表，注意缩进，下文详细讲解
   deploy: git@github.com:<用户名>/<用户名>.github.io.git
   ```

#### 6. 参考文档

- [[Blog]]()
