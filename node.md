# nodejs是啥
大家都知道谷歌浏览器有个V8引擎，速度很快！

09年的时候，有个大牛，他的工作是用C/C++写高性能Web服务，对于高性能，异步IO、事件驱动是基本原则，但是用C/C++写就太痛苦了。于是这位仁兄开始设想用高级语言开发Web服务。他评估了很多种高级语言，发现很多语言虽然同时提供了同步IO和异步IO，但是开发人员一旦用了同步IO，他们就再也懒得写异步IO了，所以，最终，他瞄向了JavaScript。

选定了开发语言，还要有运行时引擎。这位仁兄曾考虑过自己写一个，不过明智地放弃了，因为V8就是开源的JavaScript引擎。让Google投资去优化V8，咱只负责改造一下拿来用，还不用付钱，这个买卖很划算。
于是在2009年，大牛正式推出了基于JavaScript语言和V8引擎的开源Web服务器项目，命名为Node.js。虽然名字不咋滴，但是，Node第一次把JavaScript带入到后端服务器开发，加上世界上已经有无数的JavaScript开发人员，所以Node一下子就火了起来。

在Node上运行的JavaScript相比其他后端开发语言有何优势？

最大的优势是借助JavaScript天生的事件驱动机制加V8高性能引擎，使编写高性能Web服务轻而易举。
JavaScript语言本身是完善的函数式语言，在Node环境下，通过模块化的JavaScript代码，加上函数式编程，并且无需考虑兼容性问题，直接使用最新的ECMAScript 6标准，可以完全满足工程上的需求。
前后端语言统一，降低开发成本

另外，有好多同学一听到 NodeJS，就会联想到这是用来写服务器的。其实nodejs可以直接访问文件系统、处理二进制数据？这意味着可以用 JavaScript 的语法来写各种各样的本地工具。其中最著名那些就是前端自动化构建工具，比如Webpack等。在很久以前，前端的概念无非是 HTML、CSS、JavaScript，当时页面的样式和交互还没有现在那么复杂，所以只需要完成基本的样式显示和数据操作就好了。但是现在，各种复杂的页面相继出现，甚至出现了 AngularJS、ReactJS、VueJS 这样的大工程。为了提高网页的加载速度，前端们不得不在发布前将所有的文件拼合在一起并混淆压缩以节省流量和请求数。所以现在各种构建工具横行，大家以后应该都会接触到。

nodejs能干啥
-	处理高并发web服务
-	实时通信应用服务
-	天猫大量使用nodejs替代php

代码示例

    `var http = require('http');
	http.createServer(function (req, res) {
	    res.writeHead(200, {'Content-Type': 'text/plain'});
	    res.end('Hello World\n');
	}).listen(80, "127.0.0.1"); `

上述代码即是用来创建一个输出Hello World的web服务，可以看出来，nodejs代码很简练，上手相对容易。
资料	
-	[官方文档](http://nodejs.cn/api/)		
-	[学习教程1](http://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501245426ad4b91f2b880464ba876a8e3043fc8ef000)	
-	[学习教程2](https://github.com/nswbmw/N-blog)	
-	[使用案例及优劣势](https://www.zhihu.com/question/19653241)	

