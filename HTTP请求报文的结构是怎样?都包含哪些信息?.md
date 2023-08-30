---
aliases: [请求报文,HTTP请求报文]
---
请求报文具体包含的信息如下:
1. 请求行:请求方法,请求资源的URL,HTTP版本等信息.
2. 首部行:包括主机域名,连接信息,用户代理等信息.
3. 实体主体:一般不使用
4. ![[IMG_0158.png]]

```
## 请求行
### 请求方法 URL HTTP版本
GET / HTTP/1.1

## 首部行
主机域名Host UserAgent浏览器的类型和版本 Accept表示浏览器可以接受的响应内容类型。
Host: www.example.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8
```
