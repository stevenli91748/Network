# [Network 面试](https://github.com/stevenli91748/Network/blob/master/Interview/README.md)

# 网络知识目录

* [网络通信基础]()
<a href="https://imgbb.com/"><img src="https://i.ibb.co/qFQZzy9/image.jpg" alt="image" border="0"></a>

* [服务器采取的网络编程模型](#服务器采取的网络编程模型)  
  * 服务器如何管理连接---操作系统的I/O 模型
    * 阻塞
    * 非阻塞
    * 同步
    * 异步
  * 服务器如何处理请求---操作系统的进程模型
    * 单进程
    * 多进程
    * 单线程
    * 多线程
 
* 分布式应用的系统间通信方式
  * 网络通信
    * 通信协议
      * TCP/IP
      * UDP/IP
      * Multicast
      * [HTTP](https://github.com/stevenli91748/Network/blob/master/HTTP/README.md)
      * Socket
      * WebSocket
    * Java NIO基础
      * BIO(Blocking-IO, 阻塞式IO)
      * NIO(Non-Blocking IO, 非阻塞式IO)
      * AIO(Async IO/NIO.2 异步IO)
  * [基于消息方式的系统间通信]()
    * Socket方式
      * 基于java包实现消息方式的系统间通信
        * TCP/IP
        * UDP/IP
        * Multicast
      * 基于开源框架实现消息方式的系统间通信
        * Netty
        * Mina(apache，基于java NIO，对外屏蔽了JavaNIO的复杂性)
        * Dubbo
    * 消息队列方式
      * java包实现消息队列方式的系统间通信
        * JMS
      * 基于开源框架实现消息队列方式的系统间通信
        * ActiveMQ
        * RocketMQ
        * RabbitMQ
  * [基于远程调用方式的系统间通信]() 
    * 基于java包实现远程调用方式的系统间通信
      * RMI(Remote Method Invocation)
      * webservice
    * 基于开源框架实现远程调用方式的系统间通信
      * Spring RMI(简单就实现RMI方式的java远程调用)
      * Apache CXF
      * Hessian
      * AXIS
   



# 服务器采取的网络编程模型

     单服务器高性能的关键之一就是服务器采取的网络编程模型，网络编程模型有如下两个关键设计点:
       
       (l）服务器如何管理连接
       (2）服务器如何处理请求

      以上两个设计点最终都和操作系统的I/O 模型及进程模型相关。
      
      (1) I/0 模型：阻塞、非阻塞、同步、异步。
      (2）进程模型：单进程、多进程、单线程,多线程。








# 有用的参考
* [如何在Windows查看自己的电脑端口被什么程序占用了](https://blog.csdn.net/lianxue1986/article/details/51811386)
* [linux如何查看某个端口被哪个程序占用了](https://blog.如何模拟超过 5 万的并发用户csdn.net/gezilan/article/details/79921059)
* [如何模拟超过 5 万的并发用户](https://blog.csdn.net/j3T9Z7H/article/details/89666686)
* [模拟百万级TCP并发](https://blog.csdn.net/u011001084/article/details/54089182)
* [深入理解非阻塞同步IO和非阻塞异步IO](https://blog.csdn.net/iter_zc/article/details/39291647)
