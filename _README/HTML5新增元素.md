



#### 9.新增input元素的type类型

1. email
2. url
3. number
4. range
5. date
6. month
7. time
8. datetime
9. datetime-local

#### 10. 新增表单相关属性

1. autofocus属性
2. placeholder属性
3. form属性
4. required属性
5. multiple属性
6. autocomplete属性
7. min属性
8. max属性
9. pattern属性
10. step属性
11. formaction属性
12. formenctype属性
13. formmethod属性
14. formnovalidate属性
15. formtarget属性
16. disabled属性
17. labels属性
18. control属性
19. backward属性
20. forward属性
21. indeterminate属性
22. width属性
23. height属性
24. maxlength属性
25. wrap属性

#### 11. 链接相关的属性

1. media属性
2. download属性
3. ping属性
4. hreflang属性
5. sizes属性
6. target属性

#### 12. 其他属性

1. start属性
2. reversed属性
3. charset属性
4. type属性
5. label属性
6. scoped属性
7. async属性
8. mainfest属性
9. defer属性
10. sandbox属性
11. seamless属性
12. srcdoc属性

#### 13. 新增事件

1. beforeprint事件
2. afterprint事件
3. resize事件
4. error事件
5. offline事件
6. online事件
7. pageshow事件
8. beforeunload事件
9. hashchange事件
10. mousewheel事件
11. scroll事件
12. input事件
13. reset事件



　微数据（Microdata）　　HTML5 定义了一个标准化方法来标记 HTML 文档主体的元数据。

对于使用过微格式（如 hCard 和 hCalendar） 的人来说，对微数据会很熟悉，但其中还有一些重要的不同之处。最重要的是，微数据将相关信息从此前微格式控制的类移到了新的 itemprop 属性中。　　

另外，此标准添加了其他能精确定义微数据格式的属性，以及一个可以直接通过程序访问微数据的方法：　　itemscope 设置微数据段的范围。　　

itemtype 提供了定义可用的具体数据格式的 URL。　　

document.getItems() 提供对顶层微数据条目的访问；此方法会返回一个 NodeList，其中包含对应于可选参数 itemType 的条目，如果没有参数，则返回所有类型。　

HTML5 中属于单独的规范和工作组的技术多项技术已经成熟，脱离了 HTML5 规范，形成自己的文档。还有其他一些，也从 HTML 脱离出来，归类为 “Web 平台”。　　

SVG　　也许归类到 HTML5 大杂烩中最奇怪的技术就要算 Scalable Vector Graphics (SVG) 了。SVG 是用 XML 定义的矢量图形语法。自从 1999 年起，就由 W3C 开始开发 SVG，因此将它作为 “新” 内容或 HTML5 一部分的一个延伸。　　但依然值得为重新发掘 SVG 而感到高兴，因为它实际推动了标准。主要浏览器的最新版本都提供或多或少的支持，而有些库，如 Raphael.js 中还有支持旧版本 Internet Explorer 的 API。　　

Web 存储　　Web Storage 规范定义了一个 API，可对 Web 浏览器的中的键-值进行连续存储。 此规范与 cookies 的功能类似，但有了很大的改进。　　存储有两种形式：sessionStorage 与 localStorage。每一个都提供了类似的方法来管理条目（setItem()、removeItem() 和 getItem()) 和清除整个存储（clear()）。Session 存储是用来保存当前浏览器会话。Local 存储用来对网站收藏或其他用户数据进行长期存储。还可以监听存储事件，以便监控存储活动并对存储活动作出响应。　　对于现在就想体验此功能的用户，Persist.js 库提供了完善的跨浏览器解决方案可在所有主要浏览器中使用 Web 存储或等效的功能。　　还有另外两个规范可与 Web Storage 同时使用：　　IndexedDB 是一个相关的绿色规范，它提供了更强大的在浏览器中长期存储数据的功能，其中包括查询数据库，更重要是，能够保存复杂对象而不仅是简单的字符串。　　

Web Workers 是功能超强的规范，它定义了能在主页运行 JavaScript 同时让用户在底层运行脚本的 API。此功能可以让开发人员将时间较长的处理任务卸载到底层进程，从而释放浏览器，可在主要环境中进行持续交互。　　文件 API　　此规范提供了操作 Web 应用程序中文件的 API。加上其他一些新兴和成熟技术，如 XMLHttpRequest、拖放和 Web Workers，File API 能够提供比目前可用技术更强大的 Web 和桌面交互功能。 与简单文件上传输入元素将文件传递给 Web 服务器进行处理或复杂的 Flash 界面不同的是，File API 允许直接访问浏览器文件数据。　

WebSocket　　WebSocket API 可以通过一个 TCP 端口在 Web 浏览器和 Web 服务器之间同时双向通讯。在实现方面，WebSocket 还可以走得更远一些，它支持最新版本 Firefox、Opera、Chrome 和 Apple Safari，但已发现的安全漏洞使得它在 Firefox 和 Opera 中默认禁用。　　服务器发送的事件　　此规范定义了一个 API，可以打开一个 HTTP 连接，以 DOM 事件形式接收来自服务器的推送通知。本规范改变了目前在固定时间间隔轮询服务器进行更新的模式，节约了大量不需要的请求和相关的处理器时间和带宽。　　

WebGL　　Web-based Graphics Library (WebGL) 增强了JavaScript，它具有在浏览器中创建三维交互图形的功能。WebGL 是 canvas HTML 元素的上下文。此规范与 2011 年 3 月推出 1.0 版，由非营利的 Khronos Group 管理。　　XMLHttpRequest Level 2　　XMLHttpRequest Level 2 规范通过一些新特性增强了核心 XMLHttpRequest 对象。其中最有趣的大概就是 Cross-Origin Resource Sharing 了，它一种绕过同源安全策略的安全方式，可以实现 XMLHttpRequest 与第三方服务器交互。目前，XMLHttpRequest 只能与相同协议的服务器通讯。

