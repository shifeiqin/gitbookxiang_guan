## Node.js {#articleHeader2}

Node.js 是一个基于Chrome JavaScript 运行时建立的一个平台， 用来方便地搭建快速的， 易于扩展的网络应用· Node.js 借助事件驱动， 非阻塞 I/O 模型变得轻量和高效， 非常适合 run across distributed devices 的 data-intensive 的实时应用。

---

&lt;!--  
 /\* Font Definitions \*/  
 @font-face  
	{font-family:Helvetica;  
	panose-1:2 11 6 4 2 2 2 2 2 4;  
	mso-font-charset:0;  
	mso-generic-font-family:swiss;  
	mso-font-pitch:variable;  
	mso-font-signature:-536859905 -1073711037 9 0 511 0;}  
@font-face  
	{font-family:宋体;  
	panose-1:2 1 6 0 3 1 1 1 1 1;  
	mso-font-alt:SimSun;  
	mso-font-charset:134;  
	mso-generic-font-family:auto;  
	mso-font-pitch:variable;  
	mso-font-signature:3 680460288 22 0 262145 0;}  
@font-face  
	{font-family:宋体;  
	panose-1:2 1 6 0 3 1 1 1 1 1;  
	mso-font-alt:SimSun;  
	mso-font-charset:134;  
	mso-generic-font-family:auto;  
	mso-font-pitch:variable;  
	mso-font-signature:3 680460288 22 0 262145 0;}  
@font-face  
	{font-family:Calibri;  
	panose-1:2 15 5 2 2 2 4 3 2 4;  
	mso-font-charset:0;  
	mso-generic-font-family:swiss;  
	mso-font-pitch:variable;  
	mso-font-signature:-520092929 1073786111 9 0 415 0;}  
@font-face  
	{font-family:"\@宋体";  
	panose-1:2 1 6 0 3 1 1 1 1 1;  
	mso-font-charset:134;  
	mso-generic-font-family:auto;  
	mso-font-pitch:variable;  
	mso-font-signature:3 680460288 22 0 262145 0;}  
 /\* Style Definitions \*/  
 p.MsoNormal, li.MsoNormal, div.MsoNormal  
	{mso-style-unhide:no;  
	mso-style-qformat:yes;  
	mso-style-parent:"";  
	margin:0cm;  
	margin-bottom:.0001pt;  
	text-align:justify;  
	text-justify:inter-ideograph;  
	mso-pagination:none;  
	font-size:10.5pt;  
	mso-bidi-font-size:11.0pt;  
	font-family:"Calibri","sans-serif";  
	mso-ascii-font-family:Calibri;  
	mso-ascii-theme-font:minor-latin;  
	mso-fareast-font-family:宋体;  
	mso-fareast-theme-font:minor-fareast;  
	mso-hansi-font-family:Calibri;  
	mso-hansi-theme-font:minor-latin;  
	mso-bidi-font-family:"Times New Roman";  
	mso-bidi-theme-font:minor-bidi;  
	mso-font-kerning:1.0pt;}  
.MsoChpDefault  
	{mso-style-type:export-only;  
	mso-default-props:yes;  
	font-family:"Calibri","sans-serif";  
	mso-bidi-font-family:"Times New Roman";  
	mso-bidi-theme-font:minor-bidi;}  
 /\* Page Definitions \*/  
 @page  
	{mso-page-border-surround-header:no;  
	mso-page-border-surround-footer:no;}  
@page WordSection1  
	{size:595.3pt 841.9pt;  
	margin:72.0pt 90.0pt 72.0pt 90.0pt;  
	mso-header-margin:42.55pt;  
	mso-footer-margin:49.6pt;  
	mso-paper-source:0;  
	layout-grid:15.6pt;}  
div.WordSection1  
	{page:WordSection1;}  
--&gt;  


先在windows下安装nodejs

官网：[https://nodejs.org/en/](file:///C:\Users\FayQ\AppData\Local\GitBook_Editor\app-7.0.12\resources\app.asar\editor.html?config=eyJzdG9yYWdlS2V5IjoiXy9RenBjVlhObGNuTmNSbUY1VVZ4SGFYUkNiMjlyWEV4cFluSmhjbmxjU1cxd2IzSjBYR2RwZEdKdmIydDRhV0Z1WjE5bmRXRnUtMTUyMjIxNjYyNTQ0OCIsImhvc3QiOiJodHRwOi8vbG9jYWxob3N0OjQ0MjQ0IiwidXNlcm5hbWUiOiJzaGlmZWlxaW4iLCJ0b2tlbiI6Im9kMmJkeGhsdGg2IiwiY29tbWl0dGVyIjp7Im5hbWUiOiJzaGlmZWlxaW4iLCJlbWFpbCI6IjEwMTAwNDY2NjBAcXEuY29tIn0sImFuYWx5dGljcyI6eyJkZWJ1ZyI6MCwiZGlzdGluY3RJRCI6IjVhYjllNmU4ZjNkZDFkMDAyZWU2M2MxMSJ9LCJib29rIjp7InRpdGxlIjoiZ2l0Ym9va3hpYW5nX2d1YW4iLCJ1cmwiOiIiLCJpZCI6bnVsbH0sImFwaSI6eyJob3N0IjoiaHR0cHM6Ly9hcGkuZ2l0Ym9vay5jb20vIiwidXNlcm5hbWUiOiJzaGlmZWlxaW4iLCJ0b2tlbiI6Im9kMmJkeGhsdGg2In0sInJlcG9zaXRvcnkiOiJfL1F6cGNWWE5sY25OY1JtRjVVVnhIYVhSQ2IyOXJYRXhwWW5KaGNubGNTVzF3YjNKMFhHZHBkR0p2YjJ0NGFXRnVaMTluZFdGdSIsInJlcG9zaXRvcnlQYXRoIjoiQzpcXFVzZXJzXFxGYXlRXFxHaXRCb29rXFxMaWJyYXJ5XFxJbXBvcnRcXGdpdGJvb2t4aWFuZ19ndWFuIn0=)

![](file:///C:\Users\FayQ\AppData\Local\Temp\msohtmlclip1\01\clip_image001.png "说明: http://images2015.cnblogs.com/blog/911086/201611/911086-20161128150200209-1564200357.png")

下载后直接安装即可

![](file:///C:\Users\FayQ\AppData\Local\Temp\msohtmlclip1\01\clip_image002.png "说明: http://images2015.cnblogs.com/blog/911086/201611/911086-20161128150331959-1136260471.png")

然后通过cmd调出DOS命令窗口测试下是否安装完成

输入命令：node

输入：console.log\("Hello,World!"\);测试一下

![](file:///C:\Users\FayQ\AppData\Local\Temp\msohtmlclip1\01\clip_image003.png "说明: http://images2015.cnblogs.com/blog/911086/201611/911086-20161128150751287-1985179846.png")

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

![](file:///C:\Users\FayQ\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png "说明: http://images2015.cnblogs.com/blog/911086/201611/911086-20161128150930490-1531084582.png")

编辑好文件后

再从DOS窗口进入你的app的文件夹，在命令窗口执行【node test.js】。这样就可以在网页上访问你的js了。访问网址[http://127.0.0.1:3000。如果你正常访问了，那么就安装成功了。](file:///C:\Users\FayQ\AppData\Local\GitBook_Editor\app-7.0.12\resources\app.asar\editor.html?config=eyJzdG9yYWdlS2V5IjoiXy9RenBjVlhObGNuTmNSbUY1VVZ4SGFYUkNiMjlyWEV4cFluSmhjbmxjU1cxd2IzSjBYR2RwZEdKdmIydDRhV0Z1WjE5bmRXRnUtMTUyMjIxNjYyNTQ0OCIsImhvc3QiOiJodHRwOi8vbG9jYWxob3N0OjQ0MjQ0IiwidXNlcm5hbWUiOiJzaGlmZWlxaW4iLCJ0b2tlbiI6Im9kMmJkeGhsdGg2IiwiY29tbWl0dGVyIjp7Im5hbWUiOiJzaGlmZWlxaW4iLCJlbWFpbCI6IjEwMTAwNDY2NjBAcXEuY29tIn0sImFuYWx5dGljcyI6eyJkZWJ1ZyI6MCwiZGlzdGluY3RJRCI6IjVhYjllNmU4ZjNkZDFkMDAyZWU2M2MxMSJ9LCJib29rIjp7InRpdGxlIjoiZ2l0Ym9va3hpYW5nX2d1YW4iLCJ1cmwiOiIiLCJpZCI6bnVsbH0sImFwaSI6eyJob3N0IjoiaHR0cHM6Ly9hcGkuZ2l0Ym9vay5jb20vIiwidXNlcm5hbWUiOiJzaGlmZWlxaW4iLCJ0b2tlbiI6Im9kMmJkeGhsdGg2In0sInJlcG9zaXRvcnkiOiJfL1F6cGNWWE5sY25OY1JtRjVVVnhIYVhSQ2IyOXJYRXhwWW5KaGNubGNTVzF3YjNKMFhHZHBkR0p2YjJ0NGFXRnVaMTluZFdGdSIsInJlcG9zaXRvcnlQYXRoIjoiQzpcXFVzZXJzXFxGYXlRXFxHaXRCb29rXFxMaWJyYXJ5XFxJbXBvcnRcXGdpdGJvb2t4aWFuZ19ndWFuIn0=)

![](file:///C:\Users\FayQ\AppData\Local\Temp\msohtmlclip1\01\clip_image005.png "说明: http://images2015.cnblogs.com/blog/911086/201611/911086-20161128151043677-1551847562.png")

![](file:///C:\Users\FayQ\AppData\Local\Temp\msohtmlclip1\01\clip_image006.png "说明: http://images2015.cnblogs.com/blog/911086/201611/911086-20161128151325990-269570167.png")

Nodejs安装成功。



