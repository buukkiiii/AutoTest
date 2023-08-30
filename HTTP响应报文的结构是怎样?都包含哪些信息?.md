
---
aliases: [HTTP响应报文,响应报文]
---
1. 状态行:HTTP版本,[[什么是HTTP状态码?都有哪些状态码?|状态码]],解释状态码短语
2. 首部行:服务器信息,时间,内容类型,内容长度
3. 实体主体:响应内容

![[IMG_0159.png]]
```
< HTTP/1.1 200 OK
< Server: nginx/1.10.2
< Date: Thu, 12 Mar 2020 09:13:44 GMT
< Content-Type: image/png
< Content-Length: 11390
< Last-Modified: Sat, 27 Jan 2018 13:51:30 GMT
< Connection: keep-alive
< ETag: "5a6c83e2-2c7e"
< Accept-Ranges: bytes
<
```