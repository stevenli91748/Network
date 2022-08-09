# [Network 面试](https://github.com/stevenli91748/Network/blob/master/Interview/README.md)

# 在线书籍
* [深入理解计算机网络---王达 20年网络经验](https://weread.qq.com/web/reader/2a3328e05934522a3f38d15)
* [5G为人工智能与工业互联网](https://weread.qq.com/web/reader/025321d071a561dc025d935)

* [19 (疯狂创客圈) Netty Zookeeper Redis 高并发实战](https://weread.qq.com/web/reader/1e732510718f63a11e7dee2)
  * [19.1 《Netty  Redis  Zookeeper 高并发实战》随书源码、说明](https://www.cnblogs.com/crazymakercircle/p/9904544.html)

* [20 (疯狂创客圈) Java高并发核心编程 (卷1)](https://weread.qq.com/web/reader/e6d323b0723b6029e6d1c55) 
  * [20.1 《Java高并发核心编程 (卷1)》随书源码、说明](https://www.cnblogs.com/crazymakercircle/p/9904544.html) 

* [21 (疯狂创客圈) Java高并发核心编程 (卷2)](https://weread.qq.com/web/reader/9b93254072456ac19b9a176)
  * [21.1 《Java高并发核心编程 (卷2)》随书源码、说明](https://www.cnblogs.com/crazymakercircle/p/9904544.html) 



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

[Java 全栈知识体系---Java IO知识体系详解](https://www.pdai.tech/md/java/io/java-io-overview.html)|
---|

[精尽计算机网络学习指南](http://svip.iocoder.cn/Net/tutorials/)|[计网 IP 知识全家桶，45 张图一套带走](https://mp.weixin.qq.com/s/21Tk-8gxpDoH9DNWNYCWmA)|[Java IO知识体系详解](https://www.pdai.tech/md/java/io/java-io-overview.html)|
---|---|---|

[Java IO知识体系详解](https://www.pdai.tech/md/java/io/java-io-overview.html)|
---|

[不了解NIO你好意思说自己是Java程序员？](https://www.bilibili.com/video/BV1fW411c7pL)|[我见过最清晰的总结，一键搞定Netty难关，看到NIO再也不犯糊涂了](https://zhuanlan.zhihu.com/p/181321048?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656)|
---|---|

[吐血整理所有常用端口，不全你来打我！](https://cloud.tencent.com/developer/article/1116094?from=article.detail.1114773)|
---|

### I/O网络通信框架的发展历程：
* [手动搭建I/O网络通信框架1：Socket和ServerSocket入门实战，实现单聊](https://www.cnblogs.com/lbhym/p/12673470.html)
* [手动搭建I/O网络通信框架2：BIO编程模型实现群聊](https://www.cnblogs.com/lbhym/p/12681787.html)
* [手动搭建I/O网络通信框架3：NIO编程模型，升级改造聊天室](https://www.cnblogs.com/lbhym/p/12698309.html)
* [手动搭建I/O网络通信框架4：AIO编程模型，聊天室终极改造](https://www.cnblogs.com/lbhym/p/12720944.html)
* [SpringBoot+Netty+WebSocket实现实时通信](https://www.cnblogs.com/lbhym/p/12497212.html)

[ServerSocket与Socket入门详解](https://blog.csdn.net/J080624/article/details/78468396)|[Socket编程实践模拟通信](https://blog.csdn.net/J080624/article/details/78468502)|
---|---|





* [网络通信基础]()
<a href="https://imgbb.com/"><img src="https://i.ibb.co/qFQZzy9/image.jpg" alt="image" border="0"></a>
* [4/7层网络模型](https://www.cnblogs.com/cac2020/p/11821299.html)

* [单服务器采取的网络编程模型原理](#单服务器采取的网络编程模型原理)  
  * [服务器如何管理连接---操作系统的I/O 模型](https://www.zhihu.com/question/19732473)
    * 阻塞
    * 非阻塞
    * 同步
    * 异步
  * 服务器如何处理请求---操作系统的进程模型
    * 单进程
    * 多进程
      * 消息传递
        * 管道
        * FIFO
        * 消息队列 
      * 同步
        * 互斥量
        * 读写锁
        * 信号量 
      * 共享内存
      * 远程过程调用 
    * 单线程
    * 多线程
  
  * 网络编程模型的实际方案
    * PPC
    * Prefork
    * TPC
    * Prethread
    * Reactor
    * Proactor
 
* 分布式应用的系统间通信方式
  * 网络通信
    * 通信协议
      * [HTTP](https://www.cnblogs.com/cac2020/p/11837066.html)
        * [HTTP github](https://github.com/stevenli91748/Network/blob/master/HTTP/README.md)
      * [HTTPS](https://www.cnblogs.com/cac2020/p/11859105.html)
      * [HTTP2](https://www.cnblogs.com/cac2020/p/11867852.html)
      * [TCP](https://www.cnblogs.com/cac2020/p/11950660.html)
      * [UDP](https://www.cnblogs.com/cac2020/p/11950679.html)
      * Multicast
      * Socket
      * WebSocket
    * [Java NIO基础](https://www.bilibili.com/video/BV1fW411c7pL)
      * [BIO(Blocking-IO, 同步阻塞式IO)](#BIO)
      * [NIO(Non-Blocking IO, 同步非阻塞式IO)](#NIO)
        * [10分钟看懂， Java NIO 底层原理---疯狂创客圈](https://www.cnblogs.com/crazymakercircle/p/10225159.html) 
      * [AIO(Async IO/NIO.2 异步非阻塞式IO)](#AIO)
  * [基于消息方式的系统间通信]()
    * [Socket方式](https://blog.csdn.net/J080624/article/details/78468396)
      * 基于java包实现消息方式的系统间通信
        * [TCP/IP协议 （图解+秒懂+史上最全）---疯狂创客圈](https://www.cnblogs.com/crazymakercircle/p/14499211.html)
        * UDP/IP
        * Multicast
      * 基于开源框架实现消息方式的系统间通信
        * [Netty](https://github.com/stevenli91748/JAVA-Architecture/blob/master/Tools%20and%20Middleware/Netty/README.md)
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

  同步阻塞⽅式（BIO），[客户端每发⼀次请求，服务端就⽣成⼀个线程去处理。当客户端同时发起的请求很多时，服务端
  需要创建很多的线程去处理每⼀个请求](https://weread.qq.com/web/reader/71d32370716443e271df020ka0a32dd027aa0a080f42962)，如果达到了系统最⼤的线程数瓶颈，新来的请求就没法处理了。


# NIO

  同步⾮阻塞⽅式 (NIO)，客户端每发⼀次请求，服务端并不是每次都创建⼀个新线程来处理，⽽是[通过I/O多路复⽤技术
  ⾏处理。就是把多个I/O的阻塞复⽤到同⼀个select的阻塞上](https://weread.qq.com/web/reader/71d32370716443e271df020ka0a32dd027aa0a080f42962)，从⽽使系统在单线程的情况下可以同时处
  理多个客户端请求。这种⽅式的优势是开销⼩，不⽤为每个请求创建⼀个线程，可以节省系统开销。

* [NIO 网络编程框架 --- Netty](https://github.com/stevenli91748/JAVA-Architecture/blob/master/Tools%20and%20Middleware/Netty/README.md)

# AIO

  异步⾮阻塞⽅式（AIO），客户端只需要发起⼀个I/O操作然后⽴即返回，等I/O操作真正完成以后，客户端会得到I/O操作完
  成的通知，此时客户端只需要对数据进⾏处理就好了，不需要进⾏实际的I/O读写操作，因为真正的I/O读取或者写⼊操作已
  经由内核完成了。这种⽅式的优势是客户端⽆需等待，不存在阻塞等待问题。

* [AIO 网络编程框架--- t-io](https://gitee.com/sxhjlzl/t-io)




# 网络视频
 * [Computer Networking Course - Network Engineering](https://www.youtube.com/watch?v=qiQR5rTSshw)
 * [Full Ethical Hacking Course - Network Penetration Testing for Beginners (2019)](https://www.youtube.com/watch?v=3Kq1MIfTWCE)
 * [清华大牛权威讲解nio,epoll,多路复用，更好的理解redis-netty-Kafka等热门技术](https://www.bilibili.com/video/BV11K4y1C7rm/?spm_id_from=333.788.videocard.8)
 * [HTTP协议详解](https://www.bilibili.com/video/av28681865/?spm_id_from=333.788.videocard.18)
 * [Fiddler抓包工具实战全网最全最细教程，没有之一](https://www.bilibili.com/video/av58454086/?spm_id_from=333.788.videocard.14)
 * HTTP WATCH
 * [[尚学堂]Java---网络编程/手写服务器 手写聊天室 手写Webserver](https://www.bilibili.com/video/av38603991/?spm_id_from=333.788.videocard.19)
 * [web网络服务器开发案例 socket /tcp.ip 编程（完](https://www.bilibili.com/video/av53761019/?spm_id_from=333.788.videocard.1)
 * [Linux网络编程 - 轻量级http服务器项目](https://www.bilibili.com/video/av60661105/?spm_id_from=333.788.videocard.15)
 * [2019最新Java网络编程全套教程（NIO+Tomcat+Netty+Socket）](https://www.bilibili.com/video/av78244890?from=search&seid=14264493485384835458)
 * [ Network Fundamentals ](https://www.youtube.com/watch?v=cNwEVYkx2Kk&list=PLDQaRcbiSnqF5U8ffMgZzS7fq1rHUI3Q8)
 
 
 
# 有用的参考
* [Windows：查看IP地址，IP地址对应的机器名，占用的端口，以及占用该端口的应用程](https://www.cnblogs.com/ljhdo/p/4548840.html)
* [Http 长连接、短连接、长轮询、短轮询](https://www.jianshu.com/p/22dabfef3785)
* [前端通讯协议大比拼：WebSockets和HTTP](https://juejin.cn/post/6984991337841950757)
* [了解 HTTP/1.x 的 keep-alive 吗？它与 HTTP/2 多路复用的区别是什么](https://juejin.cn/post/6989985247836241957)
* [HTTP & Session & Cookie](https://juejin.cn/post/6991098235557249032)
* [一个 TCP 连接可以发多少个 HTTP 请求](https://juejin.cn/post/6844904083703201806)
* [TCP连接、Http连接与Socket连接的区别](https://blog.csdn.net/mccand1234/article/details/91346202#comments_14243550)
* [HTTP Request 和Response---详解](https://blog.csdn.net/mccand1234/article/details/54577413)
* [太厉害了，终于有人能把TCP/IP协议讲的明明白白了](https://developer.51cto.com/art/201906/597961.htm)
* [面试/笔试第一弹 —— 计算机网络面试问题集锦](https://blog.csdn.net/justloveyou_/article/details/78303617)
* [阿里员工排查问题的工具清单，总有一款适合你](https://mp.weixin.qq.com/s?__biz=MzI0MDQ4MTM5NQ==&mid=2247487708&idx=1&sn=e6056808022c2b325a74ac68fe84bc1f&chksm=e91b75c0de6cfcd6c8eb5897c25f2fcc49b41ecc45c23a2c482dd6bba2fd035b4840a6588268&token=1092963491&lang=zh_CN#rd)
* [服务器开发中网络数据分析与故障排查经验漫谈](https://juejin.im/post/5befc8ee6fb9a04a0d567042)
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
* [ping命令用得这么6，原理知道不？图解一波！](https://mp.weixin.qq.com/s/55bbQX2-SUNe6PEI9My5fA)
* [探究：一个数据包在网络中到底是怎么游走的？](https://mp.weixin.qq.com/s/07zloKKMUl-RHN6tWqZIJQ)



