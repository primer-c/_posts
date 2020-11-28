---
date: October 21 2020 
title: Post请求及参数设置
categories: JavaScript
comment: true
---
#### 1. Post请求
（论述部分待续）
#### 2. 数据格式

1. Content-type格式

- `application/x-www-form-urlencoded`：  上传文件；
- `multipart/form-data`： 	表单提交；
- `application/json`： JSON对象数据；

#### 3. headers设置

1. Content-type格式: `application/x-www-form-urlencoded`
- 表单提交

  HTML代码
  ```html
   <form method="post">
     <input type="text" name="username">
     <input type="text" name="password">
   </form>
   ```
  JS代码
   ```js
   xhr.setRequestHeader('Content-type', 'application/x-www-form-urlencoded')
   ```

2. Content-type格式: `multipart/form-data`
- 文件传输

   HTML代码
   ```html
   <form method="post" enctype="multipart/form-data">
     <input id="file" type="file" name="file"/>
     <button id="upload" type="button">upload</button>
   </form>
   ```
  
  JS代码
   ```js
   xhr.setRequestHeader('Content-type', '/multipart/form-data')
   ```

3. Content-type格式: `application/json`
   ```js
   xhr.setRequestHeader('Content-type', 'application/json')
   ```
  
#### 4. 参数设置

1. send() 方法中发送数据；
- form表单数据发送
   ```js
   xhr.setRequestHeader('Content-type', 'application/x-www-form-urlencoded')
   xhr.send('username=Andy&age=20')
   ```
- 服务端解析请求
    ```js
    app.use(express.urlencoded())
    ```

#### 5. JSON数据的发送与接收

1. JSON数据发送
- 需要将JSON数据转换为String
    ```js
    let data = JSON.stringify({name: "Andy",age:20})
    xhr.send(data)
    ```
- 服务器需要解析接收到的String数据
    ```js
    app.use(express.json())
    ```
2. JSON数据的接收
- 需要将String数据转换为JSON数据
    ```js
    JSON.parse(xhr.responseText)
    ```

3.  源码
- 客户端JSON数据发送
    ```js
    const url = "http://localhost:3000"
    // 1. 创建对象
    const xhr = new XMLHttpRequest()
 
    // 2. 设置请求方式
    xhr.open("POST",url)
 
    // 6. 获取服务端响应数据
    xhr.onload = function(){
    let data = xhr.responseText
    console.log(data)
    }
 
    // 3. 设置请求headers
    xhr.setRequestHeader("Content-Type","application/json");
 
    // 4. 将JSON数据转换为String
    let data = JSON.stringify({name:"Andy",age:20});

    // 5. 发送请求
    xhr.send(data)
    ```



