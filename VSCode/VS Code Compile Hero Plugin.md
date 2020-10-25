---
date: October 23 2020
tags: VS Code
title: VS Code Compile Hero Plugin
comments: true
---

#### 1. VS Code 必备插件

- 自动编译：less, sass, scss, typescript, jade, pug and jsx.

#### 2. 安装插件：略

![Compile Hero](https://s1.ax1x.com/2020/10/24/BVAHtx.png)

- 编辑器右下角底部栏开关 Compile Hero 设置为: On

#### 3. 配置 Settings.json

- 配置输出目录： `assert/js/`

  ```json
  "compile-hero": {
    "disable-compile-files-on-did-save-code": false,
    "notification-toggle": false,
    "javascript-output-directory": "../assert/js/",
    "typescript-output-directory": "../assert/js/",
    "javascript-output-toggle": false,
    "sass-output-directory": "../assert/css/",
    "less-output-directory": "../assert/css/",
    "sass-output-toggle": true,
    "ignore": ["src/test.js", "*/test.scss", "**/spec/*", "**/src/**/*","*/less/*"],
  },
  ```

- Settings 配置示意图
  ![Settings](https://s1.ax1x.com/2020/10/24/BVZQ6U.png)

#### 4. 使用

- 按快捷键 (ctrl+s) 或者文件列表右键菜单选择 Compile File(s) 命令启动编译，将会在该文件的同级目录 assert/js 或者 assert/css 下生成编译后的文件，助你远离 webpack 和 gulp 等编译工具操作的繁琐；

- 按快捷键 (alt+shift+f) 或者文件列表右键菜单选择 Format Document 将会帮你自动格式化文件；

- 支持 less, scss, scss 等文件代码高亮；

- 支持在默认浏览器打开 html 文件；

- 支持压缩 javascript 和 css 文件

- 支持格式化 javascript, json, css, sass, 和 html 等文件；

- 可修改编译后目录和文件的输出位置: 文件列表点击插件 Setting =>

  ![Setting](https://s1.ax1x.com/2020/10/24/BVmwee.png)

#### 5. 参考文档

[[VS Code 安装、配置与使用]]()
