---
date: October 21 2020 
title: Ajax状态码及错误处理
categories: JavaScript
comment: true
---

#### 7. Ajax技术原理需要改进： onerror事件



#### 8. HTTP通信协议

- HTTP 协议是以 ASCII 码传输，建立在 TCP/IP 协议之上的应用层规范;
- 规范把 HTTP 请求分为三个部分：状态行、请求头、消息主体；
- 服务端根据请求头（headers）中的 Content-Type字段来对主体进行解析；

#### 9. Ajax 请求方式

1. HTTP 请求方法有： GET、POST、PUT、DELETE

- GET请求： 页面刷新、图片、HTML、CSS、JS文件、标签链接；

- GET请求传递参数

  ```js
  const url = "http://localhost:3000"
  const xhr = new XMLHttpRequest();
  let params = "username=" + username + "&age=" + age;
  xhr.open('GET',(url + "/get?" + params))
  xhr.onload = function(){
    let data = xhr.responseText
  }
  xhr.send()
  ```

2. POST请求： 

- 表单提交

- POST提交数据，包含 Content-Type 和消息主体编码方式两部分

  ```js
  const url = "http://localhost:3000"
  const xhr = new XMLHttpRequest();
  xhr.open('POST',url)
  xhr..setRequestHeader('Content-type', 'application/x-www-form-urlencoded')
  let params = "username=Andy&age=20"
  xhr.onload = function(){
    let data = xhr.responseText
  }
  xhr.send(params)
  ```

- Post请求参数设置

 [[Post请求参数设置]]()

10. 案例源码

[[Ajax异步请求案例]]()
[[Ajax异步请求案例 - JSON解析]]()

11. Ajax封装
    JavaScript封装： 参考文档
    jQuery封装： 参考文档
    Fetch封装： 参考文档
    Axios封装： 参考文档