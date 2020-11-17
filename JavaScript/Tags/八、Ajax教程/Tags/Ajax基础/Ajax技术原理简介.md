---
date: October 21 2020 
title: Ajax技术原理简介
tags: Ajax
comment: true
---
#### 1. Ajax 简介
1. Ajax: Asynchronous JavaScript and XML（异步JavaScript和XML）
2. Ajax不是一种新的编程语言，而是一种用于创建快速动态网页的技术和方法；
3. Ajax 是浏览器端进行网络编程(发送请求，接收响应)的技术方案；
4. 通过在后台与服务器进行少量数据交换，Ajax可以使网页实现异步局部更新；

#### 2. Ajax 融合技术
1. 使用 CSS 和 HTML 来渲染页面
2. 使用 DOM 模型实现交互和动态渲染
3. 使用 XMLHttpRequest 实现与服务器异步通信
4. 使用 Javascript 实现绑定和调用

#### 3. 传统网站中存在的问题
1. 网页加载的时间长，用户体验不好；
2. 表单提交后，如果某项内容不符合要求时，需要重新填写所有表单的内容；
3. 页面跳转，重新加载页面，造成资源的浪费，增加用户的等待时间；

#### 4. Ajxa 的应用
1. 页面上拉加载更多数据
2. 列表数据无需刷新分页
3. 表单项离开焦点数据验证
4. 搜索框提示文字下拉列表

#### 5. Ajax Web技术特点

1. JavaScript采用单线程工作机制，代码的执行采取排队方式依次进行；

2. 客户端代码无需等待服务端数据响应完成，代码执行采用异步操作；

3. Ajax通过创建XMLHttpRequest对象从客户端发起数据请求；

4. 服务端收到请求后，为客户端准备数据或资源；

5. 当数据准备完成，响应客户端数据；

6. 当对象状态属性为： readyState == 4 并且 statue == 200时， 返回数据完成，渲染页面；

#### 6.工作原理图

- Ajax工作原理图

  ![Ajax工作原理](https://s1.ax1x.com/2020/10/15/0TuCQA.png)

#### 7.Ajax工作原理

1. XMLHttpRequest对象

- Ajax 的核心是 XMLHttpRequest 对象
- 不同的浏览器创建 XMLHttpRequest 对象的方法存在兼容问题

2. 兼容代码

   ```js
     let xhr;
     if(window.XMLHttpRequest) {
       // 1. 标准浏览器
       xhr = new XMLHttpRequest()
     }else{
       // 2. IE 浏览器
       xhr = new ActiveXObject('Mircrosoft.XMLHTTP')
     }
   ```

- 随着现代浏览器的相互兼容，对于高版本浏览器，可以不考虑兼容问题；

3. 属性

- readyState属性： 存有服务器响应的状态信息；

- 每当 readyState 改变时，onreadystatechange 函数就会被执行；

   表一：Ajax请求状态码说明

   | 状态码（status） | 说明(Description)                                |
   | ---------------- | ------------------------------------------------ |
   | 0                | 请求未初始化，open()未执行                       |
   | 1                | 请求已提出，open()已执行，send() 之前            |
   | 2                | 请求已发送，服务端已经接收到客户端请求           |
   | 3                | 请求处理中，服务器还没有完成响应                 |
   | 4                | 请求已完成，接收到服务端数据，可以使用它渲染页面 |

- 可以向 onreadystatechange 函数添加一个 if 语句，请求响应是否完成

   ```js
   xhr.onreadystatechange = function () {
    if (xhr.readyState == 4 && xhr.status == 200) {}
   }
   ```

- response Text 属性: responseText 属性返回字符串形式的响应数据

   ```js
   xhr.onreadystatechange = function () {
     if (readyState === 4) {
      document.querySelector('div').innerHTML = xhr.responseText
     }
   }
   ```
   
- status属性： 服务器响应 HTTP 状态码

   | HTTP 状态码 | 说明(Description) |
   | ----------- | ----------------- |
   | 200         | 请求响应成功      |
   | 404         | 文件未找到        |
   | 500         | 服务器故障        |

- 属性说明

   | 属性(Attribute) | 说明(Description)                                   |
   | --------------- | --------------------------------------------------- |
   | readyState      | 详见readyState属性                                  |
   | responseText    | 详见responseText属性                                |
   | responseBody    | 服务器响应，返回响应主体                            |
   | responseStream  | 服务器响应，返回的数据流                            |
   | status          | 详见status属性                                      |
   | statusText      | 服务器响应，返回 HTTP 状态码文本(OK 或者 NOT FOUND) |

4. 事件

- onreadystatechange： 存有处理服务器响应的函数： 事件(回调函数)
- 该事件在Ajax早期使用较多，现在已经不流行了；
   ```js
   xhr.onreadystatechange = function () {
     if(xhr.readyState == 4 && xhr.status == 2){
       let data = xhr.responseText
     }
   }
   ```
- onload: 代码简单，推荐使用；
  ```js
  xhe.onload = function{
    let data = xhr.responseText
  }
  ```

- onerror事件

  

1. 方法

- open() 方法 ：提交请求

   ```js
   // 第一个参数： 请求方式
   // 第二个参数： URL
   // 第三个参数： 默认为true，表示异步请求(Async)
   xhr.open('Methods', url, true);
   ```
- send()方法：

7. 源码

- onreadystatechang事件
   ```js
    // 1. 创建XMLHttpRequest对象

    let xhr;
    if(window.XMLHttpRequest) {
      xhr = new XMLHttpRequest();
    }else{
      xhr = new ActiveXObject('Mircrosoft.XMLHTTP');
    }
    // 2. 设置请求方式
    xhr.open('Methods', url, true);
    
    //3. 发送请求

    xhr.send();

    // 4.监听事件状态属性的变化,接受服务器响应数据，渲染页面
    xhr.onreadystatechange = function () {
      if (xhr.readyState == 4 && xhr.status == 200) {
        document.querySelector('div').innerHTML = xhr.responseText;
      }
    }
   ```

- onload事件
   ```js
   // 1. 创建XMLHttpRequest对象

    const xhr = new XMLHttpRequest();
   
    // 2. 设置请求方式
    xhr.open('Methods', url);
    
    //3. 发送请求

    xhr.send(null);

    // 4.监听事件状态属性的变化,接受服务器响应数据，渲染页面
    xhr.onload = function () {
      document.querySelector('div').innerHTML = xhr.responseText;
    }
   ```
   
- onerror事件

   ```js
   
   ```

   
