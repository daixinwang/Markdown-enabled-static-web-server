---
title: HTTP协议
author: Java网络编程
date: 2022-06-01 00:50
priority: 1
---

# HTTP是什么?

HTTP(超文本传输协议)是一套在网络上传输文件(如文本、图像、声音、视频和其他多媒体文件)的规则。 
一旦用户打开他们的网页浏览器，他们就间接地使用HTTP。 HTTP是一种运行在TCP/IP协议组之上的应用协议，
这些协议构成了互联网的基础。 HTTP的最新版本是HTTP/2，发布于2015年5月。 
它是它的前身HTTP 1.1的一个替代方案，但它并没有过时。

# HTTP是如何工作的

通过HTTP协议，资源在internet上的客户端设备和服务器之间交换。 客户端设备向服务器发送加载网页所需的资源请求; 
服务器将响应发送回客户机以完成请求。 请求和响应共享子文档——例如关于图像、文本、文本布局等的数据——
这些数据由客户端web浏览器拼接在一起，以显示完整的web页面文件。  

除了它可以服务的网页文件外，web服务器还包含一个HTTP守护进程，这是一个等待HTTP请求并在它们到达时处理它们的程序。
 web浏览器是向服务器发送请求的HTTP客户端。 当浏览器用户通过键入URL或单击超文本链接“打开”web文件来输入文件请求时，
浏览器构建一个HTTP请求并将其发送到URL所指示的Internet协议地址(IP地址)。 目标服务器中的HTTP守护进程接收请求
并发送回所请求的文件或与该请求相关的文件。

一个用户想要访问juejin.com。 用户输入网址，计算机就会向承载该网址的服务器发送“GET”请求。 
该GET请求使用HTTP发送，并告诉juejin服务器用户正在寻找用于构造登录页面并提供其外观的HTML(超文本标记语言)代码。 
登录页面的文本包含在HTML响应中，但是页面的其他部分——尤其是图像和视频——由单独的HTTP请求和响应请求。 
发出的请求越多(例如，调用一个有大量图像的页面)，服务器响应这些请求和用户系统加载页面的时间就越长。  

当这些请求/响应对被发送时，它们使用TCP/IP在小数据包中减少和传输信息，这些数据包由二进制序列1和0组成。 
这些数据包通过电线、光缆和无线网络进行物理传输。  

服务器和客户机用于彼此共享数据的请求和响应由ASCII码组成。 请求说明客户端正在从服务器寻求什么信息; 
响应包含客户端浏览器将转换为网页的代码。

# HTTP请求和响应

客户机和服务器之间的每一次交互都称为消息。 HTTP消息是请求或响应。
 客户端设备向服务器提交HTTP请求，服务器通过向客户端发送HTTP响应进行响应。  

HTTP请求这是指客户机设备(如internet浏览器)向服务器请求加载网站所需的信息。 
该请求为服务器提供所需的信息，以调整其对客户机设备的响应。 每个HTTP请求都包含经过编码的数据，其信息如下:  

 - HTTP的具体版本 HTTP和HTTP/2是两个版本。  
 - 一个URL这指向网络上的资源。
 - HTTP方法这表明请求在其响应中期望从服务器接收到的特定操作。  
 - HTTP请求报头这包括数据，如什么类型的浏览器正在使用和什么数据的请求是寻求从服务器。 
 它还可以包括cookies，它显示先前从处理请求的服务器发送的信息。  
 - HTTP正文这是可选的信息，服务器需要从请求，如用户表单——用户名/密码登录，短响应和文件上传——正在提交到网站。

HTTP响应 HTTP响应消息是客户端设备从web服务器接收到的数据。 
顾名思义，响应是服务器对HTTP请求的响应。 HTTP响应中包含的信息根据服务器从请求接收到的上下文进行了调整。 
HTTP响应通常包括以下数据:

 - HTTP状态码表示请求客户端设备的状态。 响应可能指示成功、信息响应、重定向或服务器或客户端上的错误。  
 - HTTP响应头用于发送关于服务器和请求资源的信息。  
 - HTTP主体(可选) 如果一个请求是成功的，这包含请求的数据在HTML代码的形式，这是翻译成一个网页由客户端浏览器。
