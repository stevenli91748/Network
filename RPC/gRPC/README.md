

# 目录
 * [gRPC入门案例实战例子](https://weread.qq.com/web/reader/71d32370716443e271df020k2023270027b202cb962a56f)
 * [如何使用Protocol Buffers实际案例](https://weread.qq.com/web/reader/71d32370716443e271df020kda432420278da4fb5c6e9ad)
 * [gRPC概念 ](https://weread.qq.com/web/reader/71d32370716443e271df020keb132680275eb160de1d35c)
    * [gRPC的一些核心概念 ](https://weread.qq.com/web/reader/71d32370716443e271df020k5ef32bd02765ef0599381f7)
      * 服务定义---gRPC可以定义4种服务方法
        * [Unary RPCS（一元RPC）](https://weread.qq.com/web/reader/71d32370716443e271df020k07e323f027707e1cd7dc674)---客户端向服务端发送单个请求并获取单个响应，就像调用本地的的方法函数一样 
        * [Server streaming RPCs（服务端流式RPC）](https://weread.qq.com/web/reader/71d32370716443e271df020k07e323f027707e1cd7dc674)---客户端向服务端发送一个请求，并且客户端获取一个流以读取消息序列。客户端持续从流中读取消息，直至消息读取完毕
        * [Client streaming RPCs（客户端流式RPC）](https://weread.qq.com/web/reader/71d32370716443e271df020k07e323f027707e1cd7dc674)---客户端使用服务端提供的流写入消息序列，并发送给服务端。一旦完成写入消息，客户端会等待服务端读取这些消息并给出响应
        * [Bidirectional streaming RPCs（双向流式RPC）](https://weread.qq.com/web/reader/71d32370716443e271df020k07e323f027707e1cd7dc674)---客户端和服务端双方使用读写流发送消息序列。这两个流独立运行，因此客户端和服务器可以按任何顺序读取和写入。例如，服务器可以等待在写入其响应之前接收所有客户端消息，或者可以交替读取消息然后再写入消息，或读写其他组合。每个流中的消息顺序都会保留
      * 使用API---
      *  同步vs异步 ---gRPC支持同步调用和异步调用
    * [gRPC依赖于Protocol Buffers](https://weread.qq.com/web/reader/71d32370716443e271df020kda432420278da4fb5c6e9ad)
    * [gRPC相比于HTTP/JSON（RESTFul API）客户端为何在性能方面表现得如此优异 ](https://weread.qq.com/web/reader/71d32370716443e271df020kc45328f0274c45147dee704)
    * 
