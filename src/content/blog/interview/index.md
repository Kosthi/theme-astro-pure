---
title: interview
publishDate: 2025-02-05 22:00:00
description: ''
tags:
  - interview
heroImage: { src: './thumbnail.jpg', color: '#B4C6DA' }
language: '中文'
---

## 在浏览器中输⼊URL并按下回⻋之后会发⽣什么

1.输入 URL 并解析，浏览器会解析出协议，主机，端口，路径等信息，并构造一个HTTP请求，浏览器会根据请求头判断是否有HTTP缓存，如果缓存存在，则从缓存获取资源，否则从服务器上获取。

2.在发送HTTP请求之前，浏览器想要知道访问网页URL对应的IP地址，就会使用DNS域名解析得到IP地址。

3.客户端与服务器之间进行HTTP请求和HTTP响应的过程中，需要通过三次握手建立TCP连接。

4.浏览器发送HTTP/HTTPS请求到WEB服务器。

5.服务器接受HTTP请求并传递给请求处理程序并发送HTTP响应报文（请求的网页内容，状态码，压缩类型，如何缓存页面，设置的cookie）。

6.浏览器渲染页面。

7.四次挥手断开TCP连接。
