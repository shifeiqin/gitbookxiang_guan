## Node.js {#articleHeader2}

Node.js 是一个基于Chrome JavaScript 运行时建立的一个平台， 用来方便地搭建快速的， 易于扩展的网络应用· Node.js 借助事件驱动， 非阻塞 I/O 模型变得轻量和高效， 非常适合 run across distributed devices 的 data-intensive 的实时应用。

---

先在windows 下安装nodejs

官网：[https://nodejs.org/en/](https://nodejs.org/en/)

![](http://images2015.cnblogs.com/blog/911086/201611/911086-20161128150200209-1564200357.png)

下载后直接安装即可

![](http://images2015.cnblogs.com/blog/911086/201611/911086-20161128150331959-1136260471.png)

然后通过cmd调出DOS命令窗口测试下是否安装完成

输入命令：node

输入：  
console.log\("Hello,World!"\);  
测试一下

![](http://images2015.cnblogs.com/blog/911086/201611/911086-20161128150751287-1985179846.png)

在D盘下建立一个app文件夹，app文件夹里面写一个test.js。

代码如下：

var http = require\("http"\);

http.createServer\(function\(req, res\) {

res.writeHead\( 200 , {"Content-Type":"text/html"}\);

res.write\("&lt;h1&gt;Node.js&lt;/h1&gt;"\);

res.write\("&lt;p&gt;Hello World&lt;/p&gt;"\);

res.end\("&lt;p&gt;beyondweb.cn&lt;/p&gt;"\);

}\).listen\(3000\);

console.log\("HTTP server is listening at port 3000."\);

![](http://images2015.cnblogs.com/blog/911086/201611/911086-20161128150930490-1531084582.png)

编辑好文件后

再从DOS窗口进入你的app的文件夹，在命令窗口执行【node test.js】。这样就可以在网页上访问你的js了。访问网址[http://127.0.0.1:3000。如果你正常访问了，那么就安装成功了。](http://127.0.0.1:3000。如果你正常访问了，那么就安装成功了。)

![](http://images2015.cnblogs.com/blog/911086/201611/911086-20161128151043677-1551847562.png)

![](http://images2015.cnblogs.com/blog/911086/201611/911086-20161128151325990-269570167.png)

Nodejs安装成功。

