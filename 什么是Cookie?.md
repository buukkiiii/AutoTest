---
aliases: [Cookie,]
---
Cookie是基于[[什么是HTTP?|HTTP]]协议的一种用于在客户端（浏览器）和服务器之间传递和存储数据的机制，它主要用于保存用户状态和实现持久性会话。

<u>其本质是一个保存在浏览器上的包含多个键值对的数据结构.</u>
在用户访问网站时，服务器可以通过设置HTTP响应头部中的`Set-Cookie`字段，
来请求浏览器更新对应Cookie的值，从而实现各种功能。

### 工作流程:
1. 用户访问网站时，服务器会在HTTP响应[[什么叫做报文?|报文]]中使用**Set-Cookie**字段来设置浏览器的Cookie。
2. 浏览器接收到响应报文后，根据**Set-Cookie**字段的内容，设置Cookie的值。
3. 当用户再次访问同一域名或子域名时，浏览器会自动在请求的HTTP头部中添加一个**Cookie**字段，将之前存储的Cookie值发送给服务器。
4. 服务器在收到请求时，会根据**Cookie**中的信息来执行对应的操作。
![[IMG_0160.png]]

### Cookie 键值对:
1. **名称（Name）**: Cookie的标识符，用于在服务器和浏览器之间识别特定的数据项。
2. **值（Value）**: 与Cookie名称关联的具体数据。这可以是字符串、数字或其他类型的信息。
3. **域（Domain）**: 指定Cookie所属的域名。Cookie将仅在指定的域及其子域名下可见和可用。
4. **路径（Path）**: 指定Cookie的可见路径。只有在匹配指定路径的请求中，浏览器才会发送这个Cookie。
5. **过期时间（Expires / Max-Age）**: 指定Cookie的过期时间。一旦过期，浏览器将不再发送这个Cookie给服务器。如果没有设置过期时间，那么Cookie将成为会话Cookie，只在用户会话期间有效。
6. **安全性（Secure）**: 如果设置了安全标志，那么浏览器只会在通过加密的 HTTPS 连接发送这个Cookie。
7. **HttpOnly**: 如果设置了HttpOnly标志，JavaScript将无法访问这个Cookie，从而提高安全性。
8. **SameSite**: 控制Cookie在跨站点请求时是否发送。可以是`Strict`、`Lax`或`None`。
9. SessionID:用来存储[[什么是session?|Session]] ID，以便实现Session的跟踪。
<!--ID: 1693151867259-->
