## Node.js {#articleHeader2}

Node.js 是一个基于Chrome JavaScript 运行时建立的一个平台， 用来方便地搭建快速的， 易于扩展的网络应用· Node.js 借助事件驱动， 非阻塞 I/O 模型变得轻量和高效， 非常适合 run across distributed devices 的 data-intensive 的实时应用。

---

先在windows下安装nodejs

官网：[https://nodejs.org/en/](file:///C:\Users\FayQ\AppData\Local\GitBook_Editor\app-7.0.12\resources\app.asar\editor.html?config=eyJzdG9yYWdlS2V5IjoiXy9RenBjVlhObGNuTmNSbUY1VVZ4SGFYUkNiMjlyWEV4cFluSmhjbmxjU1cxd2IzSjBYR2RwZEdKdmIydDRhV0Z1WjE5bmRXRnUtMTUyMjIxNjYyNTQ0OCIsImhvc3QiOiJodHRwOi8vbG9jYWxob3N0OjQ0MjQ0IiwidXNlcm5hbWUiOiJzaGlmZWlxaW4iLCJ0b2tlbiI6Im9kMmJkeGhsdGg2IiwiY29tbWl0dGVyIjp7Im5hbWUiOiJzaGlmZWlxaW4iLCJlbWFpbCI6IjEwMTAwNDY2NjBAcXEuY29tIn0sImFuYWx5dGljcyI6eyJkZWJ1ZyI6MCwiZGlzdGluY3RJRCI6IjVhYjllNmU4ZjNkZDFkMDAyZWU2M2MxMSJ9LCJib29rIjp7InRpdGxlIjoiZ2l0Ym9va3hpYW5nX2d1YW4iLCJ1cmwiOiIiLCJpZCI6bnVsbH0sImFwaSI6eyJob3N0IjoiaHR0cHM6Ly9hcGkuZ2l0Ym9vay5jb20vIiwidXNlcm5hbWUiOiJzaGlmZWlxaW4iLCJ0b2tlbiI6Im9kMmJkeGhsdGg2In0sInJlcG9zaXRvcnkiOiJfL1F6cGNWWE5sY25OY1JtRjVVVnhIYVhSQ2IyOXJYRXhwWW5KaGNubGNTVzF3YjNKMFhHZHBkR0p2YjJ0NGFXRnVaMTluZFdGdSIsInJlcG9zaXRvcnlQYXRoIjoiQzpcXFVzZXJzXFxGYXlRXFxHaXRCb29rXFxMaWJyYXJ5XFxJbXBvcnRcXGdpdGJvb2t4aWFuZ19ndWFuIn0=)

![](/assets/1.png)

下载后直接安装即可

![](/assets/2.png)

然后通过cmd调出DOS命令窗口测试下是否安装完成

输入命令：node

输入：console.log\("Hello,World!"\);测试一下

![](/assets/3.png)

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

![](/assets/4.png)

编辑好文件后

再从DOS窗口进入你的app的文件夹，在命令窗口执行【node test.js】。这样就可以在网页上访问你的js了。访问网址[http://127.0.0.1:3000。如果你正常访问了，那么就安装成功了。](file:///C:\Users\FayQ\AppData\Local\GitBook_Editor\app-7.0.12\resources\app.asar\editor.html?config=eyJzdG9yYWdlS2V5IjoiXy9RenBjVlhObGNuTmNSbUY1VVZ4SGFYUkNiMjlyWEV4cFluSmhjbmxjU1cxd2IzSjBYR2RwZEdKdmIydDRhV0Z1WjE5bmRXRnUtMTUyMjIxNjYyNTQ0OCIsImhvc3QiOiJodHRwOi8vbG9jYWxob3N0OjQ0MjQ0IiwidXNlcm5hbWUiOiJzaGlmZWlxaW4iLCJ0b2tlbiI6Im9kMmJkeGhsdGg2IiwiY29tbWl0dGVyIjp7Im5hbWUiOiJzaGlmZWlxaW4iLCJlbWFpbCI6IjEwMTAwNDY2NjBAcXEuY29tIn0sImFuYWx5dGljcyI6eyJkZWJ1ZyI6MCwiZGlzdGluY3RJRCI6IjVhYjllNmU4ZjNkZDFkMDAyZWU2M2MxMSJ9LCJib29rIjp7InRpdGxlIjoiZ2l0Ym9va3hpYW5nX2d1YW4iLCJ1cmwiOiIiLCJpZCI6bnVsbH0sImFwaSI6eyJob3N0IjoiaHR0cHM6Ly9hcGkuZ2l0Ym9vay5jb20vIiwidXNlcm5hbWUiOiJzaGlmZWlxaW4iLCJ0b2tlbiI6Im9kMmJkeGhsdGg2In0sInJlcG9zaXRvcnkiOiJfL1F6cGNWWE5sY25OY1JtRjVVVnhIYVhSQ2IyOXJYRXhwWW5KaGNubGNTVzF3YjNKMFhHZHBkR0p2YjJ0NGFXRnVaMTluZFdGdSIsInJlcG9zaXRvcnlQYXRoIjoiQzpcXFVzZXJzXFxGYXlRXFxHaXRCb29rXFxMaWJyYXJ5XFxJbXBvcnRcXGdpdGJvb2t4aWFuZ19ndWFuIn0=)

![](/assets/5.png)

![](/assets/6.png)

Nodejs安装成功。

