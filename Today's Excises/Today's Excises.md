---
date: november 4 2020
title: Today's Excises for november 8 ~ 15 
tags: Todat's Excises
comment: true
---
#### 1. express 服务器

- 创建express服务器

  ```js
  //1. import express
  const express = require('express')

  // 6.import path
  const path = require('path')

  //2. create express server
  const app = express()

  //5.open express static resource: public
  app.use(express.static(path.join(__dirname,'public')))

  //3.config port and listen port:3000
  const PORT = process.env.NODE_ENV || 3000
  app.listen(PORT,console.log(`Server linten on port:http://localhost:${PORT}...`))
  ```

- [[01.创建Express服务器]](https://web-oyster.github.io/2020/10/28/Node/Express/Tags/01.%E5%88%9B%E5%BB%BAExpress%20%E6%9C%8D%E5%8A%A1%E5%99%A8/)

#### 2.Flex弹性布局实现居中对齐

- 盒子居中对齐

  ```css
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
  }
  ```

- 参考文档

[[3d_animation]](https://github.com/web-oyster/3d_animation)之3.CSS代码

#### 3. VS Code 安装 Compile Hero Pro

- 参考文档

[[sunbutton-master]](https://github.com/web-oyster/animation-master/tree/main/sunbutton-master)

#### 4. Vue框架使用

- 参考文档

[[2. 3D Magic Cube for Vue]](https://github.com/web-oyster/3d_animation/blob/main/README.md)

#### 5.Git克隆项目

- 参考文档

[[2.快速创建 Github 远程仓库]](https://web-oyster.github.io/2020/10/25/Git/Remote%20Repostories/%E5%BF%AB%E9%80%9F%E5%88%9B%E5%BB%BAGithub%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93/)

#### 4.联系方式

[[Email]](yuanmin8888@outlook.com)
