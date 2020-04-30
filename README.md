# [Network 面试](https://github.com/stevenli91748/Network/blob/master/Interview/README.md)

# 网络知识目录

<a href="https://ibb.co/N3KF4N9"><img src="https://i.ibb.co/QcMJ5HP/net151954.png" alt="net151954" border="0"></a>

# java网络编程的学习路线：

      在理解了Java并发编程技术后再看网络编程，
      1. 首先要对计算机网络有一定的了解（TCP/IP, HTTP相关知识点）
      2. 其次要了解Socket的使用及原理，
      3. 然后再去了解NIO的相关API，
      4. 多写一些客户端和服务端通迅的DEMO，
      5. 为了更好理解网络编程，还要去了解UNIX网络编程模型，这是不管使用Java或c++，都必须要了解的
      6. 为了更好理解Java网络编程需要，需要了解TOMCAT的实现原理
      7. Netty也必须了解，并用这一网络框架进行编程，还可以看看它的源码

* [网络通信基础]()
<a href="https://imgbb.com/"><img src="https://i.ibb.co/qFQZzy9/image.jpg" alt="image" border="0"></a>

* [单服务器采取的网络编程模型原理](#单服务器采取的网络编程模型原理)  
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
  
  * 网络编程模型的实际方案
    * [PPC]()
    * Prefork
    * TPC
    * Prethread
    * Reactor
    * Proactor
 
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
      * [BIO(Blocking-IO, 阻塞式IO)](#BIO)
      * [NIO(Non-Blocking IO, 非阻塞式IO)](#NIO)
      * [AIO(Async IO/NIO.2 异步IO)](#AIO)
  * [基于消息方式的系统间通信]()
    * [Socket方式](https://blog.csdn.net/J080624/article/details/78468396)
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
   * []()



# 单服务器采取的网络编程模型原理

     单服务器高性能的关键之一就是服务器采取的网络编程模型，网络编程模型有如下两个关键设计点:
       
       (l）服务器如何管理连接
       (2）服务器如何处理请求

      以上两个设计点最终都和操作系统的I/O 模型及进程模型相关。
      
      (1) I/0 模型：阻塞、非阻塞、同步、异步。
      (2）进程模型：单进程、多进程、单线程,多线程。

# BIO

     同步阻塞⽅式（BIO），客户端每发⼀次请求，服务端就⽣成⼀个线程去处理。当客户端同时发起的请求很多时，服务端
     需要创建很多的线程去处理每⼀个请求，如果达到了系统最⼤的线程数瓶颈，新来的请求就没法处理了。


# NIO

     同步⾮阻塞⽅式 (NIO)，客户端每发⼀次请求，服务端并不是每次都创建⼀个新线程来处理，⽽是通过I/O多路复⽤技术
     ⾏处理。就是把多个I/O的阻塞复⽤到同⼀个select的阻塞上，从⽽使系统在单线程的情况下可以同时处理多个客户端请
     求。这种⽅式的优势是开销⼩，不⽤为每个请求创建⼀个线程，可以节省系统开销。

# AIO

     异步⾮阻塞⽅式（AIO），客户端只需要发起⼀个I/O操作然后⽴即返回，等I/O操作真正完成以后，客户端会得到I/O操作完
     成的通知，此时客户端只需要对数据进⾏处理就好了，不需要进⾏实际的I/O读写操作，因为真正的I/O读取或者写⼊操作已
     经由内核完成了。这种⽅式的优势是客户端⽆需等待，不存在阻塞等待问题。

[ServerSocket与Socket入门详解](https://blog.csdn.net/J080624/article/details/78468396)|[Socket编程实践模拟通信](https://blog.csdn.net/J080624/article/details/78468502)|
---|---|


# 网络视频
 * [HTTP协议详解](https://www.bilibili.com/video/av28681865/?spm_id_from=333.788.videocard.18)
 * [Fiddler抓包工具实战全网最全最细教程，没有之一](https://www.bilibili.com/video/av58454086/?spm_id_from=333.788.videocard.14)
 * [HTTP WATCH]()
 * [[尚学堂]Java---网络编程/手写服务器 手写聊天室 手写Webserver](https://www.bilibili.com/video/av38603991/?spm_id_from=333.788.videocard.19)
 * [web网络服务器开发案例 socket /tcp.ip 编程（完](https://www.bilibili.com/video/av53761019/?spm_id_from=333.788.videocard.1)
 * [Linux网络编程 - 轻量级http服务器项目](https://www.bilibili.com/video/av60661105/?spm_id_from=333.788.videocard.15)
 * [2019最新Java网络编程全套教程（NIO+Tomcat+Netty+Socket）](https://www.bilibili.com/video/av78244890?from=search&seid=14264493485384835458)
 * [ Network Fundamentals ](https://www.youtube.com/watch?v=cNwEVYkx2Kk&list=PLDQaRcbiSnqF5U8ffMgZzS7fq1rHUI3Q8)
 
 
 
# 有用的参考
* [Java从网络编程到高并发学习路线](https://coding.imooc.com/learningpath/route?pathId=11)
* [TCP的三次握手、四次挥手--非常详细讲解](https://blog.csdn.net/smileiam/article/details/78226816)
* [TCP的三次握手与四次挥手理解及面试题（很全面](https://blog.csdn.net/qq_38950316/article/details/81087809?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1)
* [如何在Windows查看自己的电脑端口被什么程序占用了](https://blog.csdn.net/lianxue1986/article/details/51811386)
* [linux如何查看某个端口被哪个程序占用了](https://blog.如何模拟超过 5 万的并发用户csdn.net/gezilan/article/details/79921059)
* [如何模拟超过 5 万的并发用户](https://blog.csdn.net/j3T9Z7H/article/details/89666686)
* [模拟百万级TCP并发](https://blog.csdn.net/u011001084/article/details/54089182)
* [深入理解非阻塞同步IO和非阻塞异步IO](https://blog.csdn.net/iter_zc/article/details/39291647)

* [java网络编程的学习路线](https://github.com/stevenli91748/JAVA-Architecture/blob/master/internet%20architecture/Network%20Programming.md)
* [Java TCP/IP Socket 编程学习笔记系列](https://blog.csdn.net/mmc_maodun/column/info/socket)

* [Java IO Tutorial](http://tutorials.jenkov.com/java-io/index.html)
* [Java NIO 系列教程](http://ifeve.com/java-nio-all/)
* [Multithreaded Servers in Java](http://tutorials.jenkov.com/java-multithreaded-servers/index.html)

* [Java网络教程-基础](http://ifeve.com/java-networking/)
* [Java网络教程之Socket](http://ifeve.com/java-socket/)
* [Java 网络教程: ServerSocket](http://ifeve.com/java-network-serversocket-2/)
* [Java Networking: UDP DatagramSocket](http://tutorials.jenkov.com/java-networking/udp-datagram-sockets.html)
* [Java网络教程:URL + URLConnection](http://ifeve.com/java-netword-url-urlconnection/)
* [Java网络教程:JarURLConnection](http://ifeve.com/java-jarurlconnection/)
* [Java 网络教程: InetAddress](http://ifeve.com/java-inetaddress-2/)
* [Java网络教程：Protocol Design](http://ifeve.com/java-network-protocol-design/)

