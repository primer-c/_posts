---
date: October 28 2020
categories: Node
title: Express服务器教程
commits: true
---

#### 1. 安装服务器： server.js

- 创建项目目录: `linux`示范

   ```bash
   touch server
   cd server
   ```

- 安装： `express`

  ```bash
  npm install express
  ```
- 根目录创建目录： routes，controls，models， configs，public，views，static

- 根目录创建文件： server.js， route.js

#### 2.配置服务器

- server.js

  ```js
  //1. 引入express安装包
  const express = require('express')

  //2. 创建服务
  const app = express()

  //3. 配置服务器端口
  const port = process.env.NODE_ENV || 3000

  //4. 监听端口： localhost:3000
  app.listen(port,() => console.log(`Express Server is running at port:http://localhost:${port}!...`))
  ```

#### 2.路由

- 配置路由

  ```js
  const routes = require('./config/routes')
  routes(app)
  ```

#### 3.静态资源

- 配置静态资源

  ```js
  //1. 引入path包
  const path = require('path')

  //2. 配置静态资源
  app.use(express.static(path.join(__dirname,'/public')))
  ```

#### 4. 配置模板引擎：jade.js

- 安装：` jade`

```js
//1. 引入jade包
const jade=require("jade");   

//2. 设置默认的模板引擎
app.set("view engine","jade");   

//3. 定义模板引擎
app.engine('jade', jade.__express);     
```

#### 5.配置视图的对应目录

```js
app.set('views',path.join(__dirname,'/views'))    
```

#### 6. 配置post请求解析

```js
app.use(express.urlencoded({ extended: false }))
app.use(express.json())
```

#### 7. 安装/配置multiparty中间件：解析文件

- multiparty可以设置上传文件的保存路径、限制文件的大小...

- 对于涉及文件上传的表单，必须设置<form enctype="multipart/form-data">

  ```js
  const multipart = require('connect-multiparty');

  const multipartMiddleware = multipart();
  
  router.post('/', multipartMiddleware, async(req, res) => {
    await res.json({
      data:req.files
    })
  });

  ```

#### 8. 配置mongoose链接

```js
const connect = require('./config/connect')
```

#### 9. 安装/配置cookies: (key/value)

- 详见： Cookies 安装与配置

  ```js
  const cookieParser=require("cookie-parser")

  const session = require('express-session')

  app.use(cookieParser())

  app.use(session({
    cookieName: 'session',
    secret: 'random_string_goes_here',
    duration: 30 * 60 * 1000,
    activeDuration: 5 * 60 * 1000,
  }))  
  ```

#### 10. 安装 / 配置express-session / connect-mongo

- session

  ```js
  const session = require('express-session')

  const MongoStore = require('connect-mongo')(session)

  // 一、配置方案
  app.use(session({
    //1.服务器生成session的签名，可以是任意字符串，用于加密
    secret:'1234',

    //2.强制保存session，即使没有变化，默认值为true  
    resave:false, 

    //3.强制将未初始化的session存储，默认为true    
    saveUninitialized:true,

    //4.设置cookie，maxAge、path、domain...  
    cookie: { maxAge:1000*60*30 }, 

    //5. 默认false，每次请求时强行设置cookie，这将会重置cookie过期时间 
    rooling:true,                   
    store:new MongoStore({
      //6. 数据库地址
      url: 'mongodb://127.0.0.1:27017/student',  
      touchAfter: 24*3600,   
    })
  })) 
  ```

#### 11. 跨域

- Cors插件

  ```js
  require('cors')()
  ```

#### 12.参考文档

[[]]()

#### 13. 联系方式

[[Email]](yuanmin8888@outlook.com)
