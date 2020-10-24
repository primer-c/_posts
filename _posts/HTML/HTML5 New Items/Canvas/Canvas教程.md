# Canvas

> canvas 最早由 Apple 引入 WebKit,用于 Mac OS X 的 Dashboard,后来又在 Safari 和 Google Chrome 被实现。
> 基于 Gecko 1.8 的浏览器,比如 Firefox 1.5, 同样支持这个元素。  
> &lt;canvas&gt; 元素是 WhatWG Web applications 1.0 规范的一部分,也包含于 HTML 5 中。

### 体验 Canvas

#### 什么是 Canvas？

HTML5 的 canvas 元素使用 JavaScript 在网页上绘制图像。  
画布是一个矩形区域，您可以控制其每一像素。  
canvas 拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法。

#### 创建 Canvas 元素

向 HTML5 页面添加 canvas 元素。  
规定元素的 id、宽度和高度：

```html
<canvas id="myCanvas" width="200" height="100"></canvas>
```

#### Canvas 坐标系

![](images/location.jpg)

#### 通过 JavaScript 来绘制

```javascript
/*获取元素*/
var myCanvas = document.querySelector("#myCanvas");
/*获取绘图工具*/
var context = myCanvas.getContext("2d");
/*设置绘图的起始位置*/
context.moveTo(100, 100);
/*绘制路径*/
context.lineTo(200, 200);
/*描边*/
context.stroke();
```

### Canvas 的基本使用

#### 图形绘制

需要理解些概念：

- 路径的概念
- 路径的绘制
  - 描边 stroke()
  - 填充 fill()  
    ![](images/path.jpg)
- 闭合路径
  - 手动闭合
  - 程序闭合 closePath()
- 填充规则(非零环绕)  
  ![](images/zero.jpg)
- 开启新的路径 beginPath()

#### 设置样式

- 画笔的状态
  - lineWidth 线宽，默认 1px
  - lineCap 线末端类型：(butt 默认)、round、square
  - lineJoin 相交线的拐点 miter(默认)、round、bevel
  - strokeStyle 线的颜色
  - fillStyle 填充颜色
  - setLineDash() 设置虚线
  - getLineDash() 获取虚线宽度集合
  - lineDashOffset 设置虚线偏移量（负值向右偏移）

#### 实例练习

- 渐变色绘制
- 镂空的房子
- 绘制坐标网格
- 绘制坐标系
- 绘制坐标点
- 绘制折线图

#### 参考文档

- [w3school](http://www.w3school.com.cn/tags/html_ref_canvas.asp)
- [Canvas_API](https://developer.mozilla.org/zh-CN/docs/Web/API/Canvas_API/Tutorial)

### Canvas 图形绘制

#### 矩形绘制

- rect(x,y,w,h) 没有独立路径
- strokeRect(x,y,w,h) 有独立路径，不影响别的绘制
- fillRect(x,y,w,h) 有独立路径，不影响别的绘制
- clearRect(x,y,w,h) 擦除矩形区域

#### 圆弧绘制

- 弧度概念
- arc()
  - x 圆心横坐标
  - y 圆心纵坐标
  - r 半径
  - startAngle 开始角度
  - endAngle 结束角度
  - anticlockwise 是否逆时针方向绘制（默认 false 表示顺时针；true 表示逆时针）

#### 绘制文本

- ctx.font = '微软雅黑' 设置字体
- strokeText()
- fillText(text,x,y,maxWidth)
  - text 要绘制的文本
  - x,y 文本绘制的坐标（文本左下角）
  - maxWidth 设置文本最大宽度，可选参数
- ctx.textAlign 文本水平对齐方式，相对绘制坐标来说的
  - left
  - center
  - right
  - start 默认
  - end
- ctx.direction 属性 css(rtl ltr) start 和 end 于此相关
  - 如果是 ltr,start 和 left 表现一致
  - 如果是 rtl,start 和 right 表现一致
- ctx.textBaseline 设置基线（垂直对齐方式 ）
  - top 文本的基线处于文本的正上方，并且有一段距离
  - middle 文本的基线处于文本的正中间
  - bottom 文本的基线处于文本的证下方，并且有一段距离
  - hanging 文本的基线处于文本的正上方，并且和文本粘合
  - alphabetic 默认值，基线处于文本的下方，并且穿过文字
  - ideographic 和 bottom 相似，但是不一样
- measureText() 获取文本宽度 obj.width

#### 实例练习

- 绘制扇形
- 绘制圆角矩形
- 绘制圆
- 绘制饼图

### 做动画

#### 绘制图片

- drawImage()
  - 三个参数 drawImage(img,x,y)
    - img 图片对象、canvas 对象、video 对象
    - x,y 图片绘制的左上角
  - 五个参数 drawImage(img,x,y,w,h)
    - img 图片对象、canvas 对象、video 对象
    - x,y 图片绘制的左上角
    - w,h 图片绘制尺寸设置(图片缩放，不是截取)
  - 九个参数 drawImage(img,x,y,w,h,x1,y1,w1,h1)
    - img 图片对象、canvas 对象、video 对象
    - x,y,w,h 图片中的一个矩形区域
    - x1,y1,w1,h1 画布中的一个矩形区域

#### 序列帧动画

- 绘制精灵图
- 动起来
- 控制边界
- 键盘控制

#### 坐标变换

- 平移 移动画布的原点
  - translate(x,y) 参数表示移动目标点的坐标
- 缩放
  - scale(x,y) 参数表示宽高的缩放比例
- 旋转
  - rotate(angle) 参数表示旋转角度

### 颜色、样式和阴影

| 属性                                                                      | 描述                                     |
| :------------------------------------------------------------------------ | :--------------------------------------- |
| [fillStyle](http://www.w3school.com.cn/tags/canvas_fillstyle.asp)         | 设置或返回用于填充绘画的颜色、渐变或模式 |
| [strokeStyle](http://www.w3school.com.cn/tags/canvas_strokestyle.asp)     | 设置或返回用于笔触的颜色、渐变或模式     |
| [shadowColor](http://www.w3school.com.cn/tags/canvas_shadowcolor.asp)     | 设置或返回用于阴影的颜色                 |
| [shadowBlur](http://www.w3school.com.cn/tags/canvas_shadowblur.asp)       | 设置或返回用于阴影的模糊级别             |
| [shadowOffsetX](http://www.w3school.com.cn/tags/canvas_shadowoffsetx.asp) | 设置或返回阴影距形状的水平距离           |
| [shadowOffsetY](http://www.w3school.com.cn/tags/canvas_shadowoffsety.asp) | 设置或返回阴影距形状的垂直距离           |

| 方法                                                                                      | 描述                                    |
| :---------------------------------------------------------------------------------------- | :-------------------------------------- |
| [createLinearGradient()](http://www.w3school.com.cn/tags/canvas_createlineargradient.asp) | 创建线性渐变（用在画布内容上）          |
| [createPattern()](http://www.w3school.com.cn/tags/canvas_createpattern.asp)               | 在指定的方向上重复指定的元素            |
| [createRadialGradient()](http://www.w3school.com.cn/tags/canvas_createradialgradient.asp) | 创建放射状/环形的渐变（用在画布内容上） |
| [addColorStop()](http://www.w3school.com.cn/tags/canvas_addcolorstop.asp)                 | 规定渐变对象中的颜色和停止位置          |

### 线条样式

| 属性                                                                | 描述                                     |
| :------------------------------------------------------------------ | :--------------------------------------- |
| [lineCap](http://www.w3school.com.cn/tags/canvas_linecap.asp)       | 设置或返回线条的结束端点样式             |
| [lineJoin](http://www.w3school.com.cn/tags/canvas_linejoin.asp)     | 设置或返回两条线相交时，所创建的拐角类型 |
| [lineWidth](http://www.w3school.com.cn/tags/canvas_linewidth.asp)   | 设置或返回当前的线条宽度                 |
| [miterLimit](http://www.w3school.com.cn/tags/canvas_miterlimit.asp) | 设置或返回最大斜接长度                   |

### 矩形

| 方法                                                                  | 描述                         |
| :-------------------------------------------------------------------- | :--------------------------- |
| [rect()](http://www.w3school.com.cn/tags/canvas_rect.asp)             | 创建矩形                     |
| [fillRect()](http://www.w3school.com.cn/tags/canvas_fillrect.asp)     | 绘制“被填充”的矩形           |
| [strokeRect()](http://www.w3school.com.cn/tags/canvas_strokerect.asp) | 绘制矩形（无填充）           |
| [clearRect()](http://www.w3school.com.cn/tags/canvas_clearrect.asp)   | 在给定的矩形内清除指定的像素 |

### 路径

| 方法                                                                              | 描述                                                    |
| :-------------------------------------------------------------------------------- | :------------------------------------------------------ |
| [fill()](http://www.w3school.com.cn/tags/canvas_fill.asp)                         | 填充当前绘图（路径）                                    |
| [stroke()](http://www.w3school.com.cn/tags/canvas_stroke.asp)                     | 绘制已定义的路径                                        |
| [beginPath()](http://www.w3school.com.cn/tags/canvas_beginpath.asp)               | 起始一条路径，或重置当前路径                            |
| [moveTo()](http://www.w3school.com.cn/tags/canvas_moveto.asp)                     | 把路径移动到画布中的指定点，不创建线条                  |
| [closePath()](http://www.w3school.com.cn/tags/canvas_closepath.asp)               | 创建从当前点回到起始点的路径                            |
| [lineTo()](http://www.w3school.com.cn/tags/canvas_lineto.asp)                     | 添加一个新点，然后在画布中创建从该点到最后指定点的线条  |
| [clip()](http://www.w3school.com.cn/tags/canvas_clip.asp)                         | 从原始画布剪切任意形状和尺寸的区域                      |
| [quadraticCurveTo()](http://www.w3school.com.cn/tags/canvas_quadraticcurveto.asp) | 创建二次贝塞尔曲线                                      |
| [bezierCurveTo()](http://www.w3school.com.cn/tags/canvas_beziercurveto.asp)       | 创建三次方贝塞尔曲线                                    |
| [arc()](http://www.w3school.com.cn/tags/canvas_arc.asp)                           | 创建弧/曲线（用于创建圆形或部分圆）                     |
| [arcTo()](http://www.w3school.com.cn/tags/canvas_arcto.asp)                       | 创建两切线之间的弧/曲线                                 |
| [isPointInPath()](http://www.w3school.com.cn/tags/canvas_ispointinpath.asp)       | 如果指定的点位于当前路径中，则返回 true，否则返回 false |

### 转换

| 方法                                                                      | 描述                                           |
| :------------------------------------------------------------------------ | :--------------------------------------------- |
| [scale()](http://www.w3school.com.cn/tags/canvas_scale.asp)               | 缩放当前绘图至更大或更小                       |
| [rotate()](http://www.w3school.com.cn/tags/canvas_rotate.asp)             | 旋转当前绘图                                   |
| [translate()](http://www.w3school.com.cn/tags/canvas_translate.asp)       | 重新映射画布上的 (0,0) 位置                    |
| [transform()](http://www.w3school.com.cn/tags/canvas_transform.asp)       | 替换绘图的当前转换矩阵                         |
| [setTransform()](http://www.w3school.com.cn/tags/canvas_settransform.asp) | 将当前转换重置为单位矩阵。然后运行 transform() |

### 文本

| 属性                                                                    | 描述                                     |
| :---------------------------------------------------------------------- | :--------------------------------------- |
| [font](http://www.w3school.com.cn/tags/canvas_font.asp)                 | 设置或返回文本内容的当前字体属性         |
| [textAlign](http://www.w3school.com.cn/tags/canvas_textalign.asp)       | 设置或返回文本内容的当前对齐方式         |
| [textBaseline](http://www.w3school.com.cn/tags/canvas_textbaseline.asp) | 设置或返回在绘制文本时使用的当前文本基线 |

| 方法                                                                    | 描述                       |
| :---------------------------------------------------------------------- | :------------------------- |
| [fillText()](http://www.w3school.com.cn/tags/canvas_filltext.asp)       | 在画布上绘制“被填充的”文本 |
| [strokeText()](http://www.w3school.com.cn/tags/canvas_stroketext.asp)   | 在画布上绘制文本（无填充） |
| [measureText()](http://www.w3school.com.cn/tags/canvas_measuretext.asp) | 返回包含指定文本宽度的对象 |

### 图像绘制

| 方法                                                                | 描述                         |
| :------------------------------------------------------------------ | :--------------------------- |
| [drawImage()](http://www.w3school.com.cn/tags/canvas_drawimage.asp) | 向画布上绘制图像、画布或视频 |

### 像素操作

| 属性                                                                  | 描述                                                |
| :-------------------------------------------------------------------- | :-------------------------------------------------- |
| [width](http://www.w3school.com.cn/tags/canvas_imagedata_width.asp)   | 返回 ImageData 对象的宽度                           |
| [height](http://www.w3school.com.cn/tags/canvas_imagedata_height.asp) | 返回 ImageData 对象的高度                           |
| [data](http://www.w3school.com.cn/tags/canvas_imagedata_data.asp)     | 返回一个对象，其包含指定的 ImageData 对象的图像数据 |

| 方法                                                                            | 描述                                                      |
| :------------------------------------------------------------------------------ | :-------------------------------------------------------- |
| [createImageData()](http://www.w3school.com.cn/tags/canvas_createimagedata.asp) | 创建新的、空白的 ImageData 对象                           |
| [getImageData()](http://www.w3school.com.cn/tags/canvas_getimagedata.asp)       | 返回 ImageData 对象，该对象为画布上指定的矩形复制像素数据 |
| [putImageData()](http://www.w3school.com.cn/tags/canvas_putimagedata.asp)       | 把图像数据（从指定的 ImageData 对象）放回画布上           |

### 合成

| 属性                                                                                            | 描述                                   |
| :---------------------------------------------------------------------------------------------- | :------------------------------------- |
| [globalAlpha](http://www.w3school.com.cn/tags/canvas_globalalpha.asp)                           | 设置或返回绘图的当前 alpha 或透明值    |
| [globalCompositeOperation](http://www.w3school.com.cn/tags/canvas_globalcompositeoperation.asp) | 设置或返回新图像如何绘制到已有的图像上 |

### 其他

| 方法          | 描述                           |
| :------------ | :----------------------------- |
| save()        | 保存当前环境的状态             |
| restore()     | 返回之前保存过的路径状态和属性 |
| createEvent() |                                |
| getContext()  |                                |
| toDataURL()   |                                |

​
