---
aliases: TCP/IP四层模型
---
![[IMG_0155.png]]

[[什么是TCP?|TCP]]/IP四层模型,是网络的基础通信架构,是OSI七层模型的一个简化版
并且在实际使用中,一般都是使用TCP/IP四层模型

1. **链路层（网络接口层）**：
    - 这一层负责管理数据在物理介质上的传输，如网线等。它处理硬件地址（MAC地址）、[[什么是帧同步?|帧同步]]以及数据的流控等任务。链路层为上面的网络层提供了一个接口，使数据帧能够在物理链路上可靠地传输。
2. **网络层**：
    - 网络层根据数据包中的目标地址来决定数据的路由。使用IP地址来标识不同的设备和网络，并根据路由表确定数据包应该通过哪些中间节点（路由器）传输，从源地址传输到目标地址。
3. **传输层**：
    - 传输层负责端到端的数据传输。它在源和目标之间的终端设备上运作，确保数据的可靠传输、流量控制以及拥塞控制等。传输层使用端口号标识不同的应用程序，以便正确地将数据传递到目标应用。
4. **应用层**：
    - 这是最接近用户的一层，负责接收数据并将其解析以呈现给用户。在应用层，各种应用协议定义了数据的格式和交换方式，如[[什么是HTTP?|HTTP]]、FTP、SMTP等，以满足不同类型的网络应用需求。

Q: 什么是TCPIP四层模型?
A: TCPIP四层模型是网络的基础通信价格,是OSI七层模型的简化版
<!--ID: 1693404822298-->


Q: TCPIP四层模型分为哪四层?每层负责什么职责?
A: 分为链路层,网络层,传输层和应用层
链路层负责数据在物理介质上的传输
网络层负责数据包的路由和转发,也就是决定数据将经由哪些网络节点传送到目标地址
传输层负责将数据完整的,可靠的传送到对端
应用层负责解析数据将结果呈现给用户
<!--ID: 1693404822301-->
