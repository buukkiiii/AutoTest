
---
aliases: [三次握手,]
---
## 字段说明
- 初始序列号ISN
	- 代表这次连接,第一个数据包的序列号,其后的数据包的序列号会在这个基础上进行递增
- 序列号(seq)
	- 某个数据包的标识
- SYN
	- 拥有两个值0,1.分别代表是否希望建立连接
- ACK
	- 拥有两个值0,1.分别代表之前的数据包是否已经成功接受
		- 之前的=从初始序列号~最近的一个序列号的数据包
- 确认号(ack)
	- 值为上一个数据包序列号的值+1,代表上一个数据包我收到了,现在我期待序列号+1的数据包

## 三次握手流程
![[Pasted image 20230823233709.png]]


Q: 说一下TCP三次握手的流程
A: 第一次请求,代表希望建立连接
第一次响应,代表服务器同意建立连接
第二次请求,代表确认了服务器的同意
<!--ID: 1693407655008-->


Q: 为什么需要第三次握手?
A: 因为第一次来自客户端的请求可能会延迟,这样在服务器收到请求并响应客户端时
客户端已经不需要建立连接了,但是由于没有第三次握手的确认,连接会被建立,服务器会浪费资源在一个不会传来数据的连接.因此需要第三次握手来建立一个可靠的连接
<!--ID: 1693407655039-->
