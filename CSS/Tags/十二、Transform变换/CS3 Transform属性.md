---
date: November 3 2020
title: 12.1 Transform 属性
tags: CSS
---

#### 1.Transform定义

1. transform 属性向元素应用 2D 或 3D 转换；
2. 该属性允许我们对元素进行旋转、缩放、移动或倾斜操作

#### 2.Transform语法

- CSS 语法
  ```css
  <selector> {
    transform: <value>
  }
  ```

- JS语法

  ```js
  object.style.transform = <value>
  ```
#### 3.Transform属性值

- 表一：属性

  |attribute|description|
  |---|---|
  |none|进行转换|
  |matrix(n,n,n,n,n,n)|2D 转换，使用六个值的矩阵|
  |matrix3d(n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n)|3D 转换，使用 16 个值的 4x4 矩阵|
  |translate(x,y)|2D 转换|
  |translate3d(x,y,z)| 3D 转换|
  |translateX(x)|定义转换，只是用 X 轴的值|
  |translateX(y)|定义转换，只是用 Y 轴的值|
  |translateZ(z)|定义转换，只是用 Z 轴的值|
  |scale(x,y)|2D 缩放转换|
  |scale3d(x,y,z)|3D 缩放转换|
  |scaleX(x)|设置 X 轴的值来定义缩放转换|
  |scaleY(y)|设置 Y 轴的值来定义缩放转换|
  |scaleZ(z)|设置 Z 轴的值来定义缩放转换|
  |rotate(angle)|2D 旋转，参数为角度|
  |rotate3d(x,y,z,angle)|3D 旋转|
  |rotateX(angle)|定义沿着 X 轴的 3D 旋转|
  |rotateY(angle)|定义沿着 Y 轴的 3D 旋转|
  |rotateZ(angle)|定义沿着 Z 轴的 3D 旋转|
  |skew(x-angle,y-angle)|沿着 X 和 Y 轴的 2D 倾斜转换|
  |skewX(angle)|沿着 X 轴的 2D 倾斜转换|
  |skewY(angle)|沿着 Y 轴的 2D 倾斜转换|
  |perspective(n)|为 3D 转换元素定义透视视图|

#### 4.案例

[[3d_animation]](https://github.com/web-oyster/3d_animation)

#### 4.参考文档

[[六、其他 CSS 属性和特性]](https://web-oyster.github.io/2020/10/28/CSS/Tutorial/%E5%85%AD%E3%80%81%E5%85%B6%E4%BB%96%20CSS%20%E5%B1%9E%E6%80%A7%E5%92%8C%E7%89%B9%E6%80%A7/)

[[十二、Transform 变换]](https://web-oyster.github.io/2020/10/28/CSS/Tutorial/%E5%8D%81%E4%BA%8C%E3%80%81%E5%8F%98%E6%8D%A2/)

#### 5. 联系方式

[[Email]](yuanmin8888@outlook.com)
