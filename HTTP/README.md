
<a href="https://ibb.co/Q6CpSBW"><img src="https://i.ibb.co/8jdNv3y/HTTP.jpg" alt="HTTP" border="0"></a>

# HTTP WATCH 10 已装在IE中， win10 平台 必须要安装 version 10以上的HTTP WATCH



# 在线书籍
* [HttpClient模块](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckeb132680275eb160de1d35c)

---



[HTTP/3详解---提供HTTP/3以及其底层协议QUIC的文档，介绍它们的目的、原理、协议细节以及实现等](https://www.kancloud.cn/kancloud/http3-explained)|[面试官：为什么要合并 HTTP 请求?](https://mp.weixin.qq.com/s/hceQ23UTHEn_T9Cr-zNAVA)|
---|---|

# 目录
* HTTP基础知识
  * [HTTP 中有八种不同的请求方式](#HTTP-中有八种不同的请求方式)
  * [影响一个HTTP网络请求的因素](#影响一个HTTP网络请求的因素)
  * [HTTP协仪各种版本的优缺点](#HTTP协仪各种版本的优缺点)
  * http报文
    * [详解http报文 1](https://juejin.cn/post/6844903956389314574)
    * [详解http报文 2-web容器是如何解析http报文的](https://juejin.cn/post/6844903959870570504) 
* [HTTP与HTTPS的区别](#HTTP与HTTPS的区别)
* [HTTP请求格式](#HTTP请求格式)
* [HTTP响应格式](#HTTP响应格式)
* [HTTP 2](https://weread.qq.com/web/reader/71d32370716443e271df020k4c5327a02794c56ff4ce24c)
     * HTTP
       * HTTP请求方法
         * 从服务器获取数据的请求
           * [GET---它是幂等（Idempotent）的，意思是发出多个相同的GET请求与发出单个GET请求具有相同的效果](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck4c5327a02794c56ff4ce24c)
             * [HttpClient模块的请求头配置 ](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka0a32dd027aa0a080f42962)
               * 添加请求头
               * 修改请求头
               * 配置请求参数 
               * [跨域访问控制](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka0a32dd027aa0a080f42962) 
                 * 跨域资源共享（CORS）
                 * 请求JSON数据---当服务器不支持跨域资源共享协议(CORS）时，JSONP是目前应用最为广泛的技术解决方案之一
                 * 请求非JSON数据 
         * 修改型的请求
           * [POST---它不是幂等的，意思是多次调用相同的POST请求与调用一次的效果不同](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc8f3245027cc8ffe9a588b8)
           * PUT---它是幂等的，意思是多次调用相同的PUT请求与调用一次的效果相同
           * PATCH
           * DELETE ---它不是幂等的，意思是多次调用相同的DELETE请求与调用一次的效果不同。
       * HTTP响应
         * [读取完整的响应信息](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka0a32dd027aa0a080f42962)
         * [ HttpClient模块与RxJS配合](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck2023270027b202cb962a56f)
           * 错误处理
           * 重试 




# 有用的参考
* [为什么请求时,需要使用URLEncode做encode转码操作](https://blog.csdn.net/u013833031/article/details/78828539)
* [Java在web页面上的编码解码处理及中文URL乱码解决](https://www.jb51.net/article/80181.htm)
* [Java 测试URL地址是否能正常连接的代码](https://www.jb51.net/article/90864.htm)
* [Java中URL传中文时乱码的解决方法](https://www.jb51.net/article/94333.htm)
* [Java HttpURLConnection超时和IO异常处理](https://www.jb51.net/article/92962.htm)
* [Java截取url参数的方法](https://www.jb51.net/article/90864.htm)
* [Java使用@Validated注解进行参数验证的方法](https://www.jb51.net/article/167642.htm)
* [java中URLEncoder.encode与URLDecoder.decode处理url特殊参数的方法](https://www.jb51.net/article/109017.htm)
* [Java如何实现URL带请求参数(get/post)及得到get和post请求url和参数列表的方法](https://www.jb51.net/article/73898.htm)
* [request请求获取参数的实现方法(post和get两种方式)]()
* [谈谈Java利用原始HttpURLConnection发送POST数据](https://www.jb51.net/article/73621.htm)
* [java使用httpclient模拟post请求和get请求示例](https://www.jb51.net/article/47282.htm)

# CORS

* [HTTP访问控制（CORS）](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Access_control_CORS)
* [一文弄懂 CORS 跨域(前端+后端代码实例讲解)](https://www.jianshu.com/p/f18388d6b931)

#  XMLHttpRequest

* [XMLHttpRequest](https://developer.mozilla.org/zh-CN/docs/Web/API/XMLHttpRequest)


# 常用的静态服务器

* [静态服务器](http://eux.baidu.com/blog/fe/%E5%B8%B8%E7%94%A8%E7%9A%84%E9%9D%99%E6%80%81%E6%9C%8D%E5%8A%A1%E5%99%A8)



# 影响一个HTTP网络请求的因素

  1. 带宽
  
  2. 延迟
     2.1  浏览器原因
     
     2.2  DNS查询
     
     2.3  建立连接
  
# HTTP 中有八种不同的请求方式
   
   [HTTP协议的8种请求类型介绍](https://www.cnblogs.com/chaoyuehedy/p/9963417.html)
   
   HTTP 中有八种不同的请求方式，包括 get、post、put、delete、option、head、trace、connect；
       
       1.  OPTIONS：允许客户端查看服务器的性能。

       2.  HEAD：类似于get请求，只不过返回的响应中没有具体的内容，用于获取报头。

       3.  GET：向特定的资源发出请求。

       4.  POST：向指定资源提交数据进行处理请求（例如提交表单或者上传文件）。数据被包含在请求体中。POST请求可能会导致新的资源的创建和/或已有资
           源的修改。

       5.  PUT：向指定资源位置上传其最新内容。

       6.  DELETE：请求服务器删除Request-URI所标识的资源。

       7.  TRACE：回显服务器收到的请求，主要用于测试或诊断。

       8.  CONNECT：HTTP/1.1协议中预留给能够将连接改为管道方式的代理服务器

# 请求提交方式
  
  默认有五种请求提交方式
  

    1. 表单请求  默认GET，可以指定POST
    
    2. AJAX请求  默认GET，可以指定POST
    
    3. 地址栏请求    （get请求）
    
    4. 超链接请求    （get请求）
    
    5. SRC资源路径请求    （get请求）

  


# HTTP与HTTPS的区别
  
  *  [http和https的区别与联系](https://www.imooc.com/article/27043)

# HTTP协仪各种版本的优缺点
 
  [HTTP1.0、HTTP1.1 和 HTTP2.0 的区别](https://www.cnblogs.com/heluan/p/8620312.html)
  
  视频
  
  [HTTP1.0  HTTP1.1  HTTP2.0的区别](https://www.bilibili.com/video/av59522356?from=search&seid=9627788764234609536)
  
  
  
   HTTP1.0
   
   HTTP1.1
   
   HTTP2.0

# HTTP请求格式

# HTTP响应格式
       

# HTTP视频

  [如何为网站配置https,非常详细的教程](https://www.bilibili.com/video/av35381918?from=search&seid=5658735684576843185)
  
  [HTTPS 网络协议原理解析](https://www.bilibili.com/video/av56542057/?spm_id_from=333.788.videocard.9)

# 有用的参考
* [99%的人都理解错了 HTTP 中 GET 与 POST 的区别](https://learnku.com/articles/25881)
* [HTTP缓存控制及为什么要缓存](https://www.chedong.com/tech/cache_docs.html)
* [硬核！30 张图解 HTTP 常见的面试题](https://mp.weixin.qq.com/s/FJGKObVnU61ve_ioejLrtw)
* [程序员：我终于知道post和get的区别](https://www.jianshu.com/p/2e2c064f1a8b)
* [为什么请求时,需要使用URLEncode做encode转码操作](https://blog.csdn.net/u013833031/article/details/78828539)
* [一文带你看清 HTTP 所有概念](https://blog.csdn.net/qq_36894974/article/details/104044932)
* [看完这篇HTTP，跟面试官扯皮就没问题了](https://blog.csdn.net/qq_36894974/article/details/103930478?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)
*  [HTTP API 设计指南（基础部分）](https://segmentfault.com/a/1190000002511720)
*  [HTTP API 设计指南（请求部分）](https://segmentfault.com/a/1190000002512493)
*  [HTTP API 设计指南（响应部分）](https://segmentfault.com/a/1190000002515342)
*  [HTTP API 设计指南（结尾）](https://segmentfault.com/a/1190000002518410)
*  [关于HTTP协议，一篇就够了](https://www.cnblogs.com/ranyonsue/p/5984001.html)
*  [HTTP----HTTP缓存机制](https://juejin.im/post/5a1d4e546fb9a0450f21af23)
*  [HTTP----HTTP2.0新特性](https://juejin.im/post/5a4dfb2ef265da43305ee2d0)
*  [HTTP----HTTP缓存机制](https://juejin.im/post/5a1d4e546fb9a0450f21af23)
*  [HTTP深入浅出](https://zhuanlan.zhihu.com/p/61469721?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656)
*  [HTTP 缓存机制](https://zhuanlan.zhihu.com/p/58685072?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656)
*  [99% 的人都理解错了 HTTP 中 GET 与 POST 的区别](https://zhuanlan.zhihu.com/p/54654014?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656)

*  [HTTP 响应代码](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Status)
*  [一个HTTP打趴80%面试者](https://zhuanlan.zhihu.com/p/60450391?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656)
* [利用负载均衡优化和加速HTTP应用](https://blog.51cto.com/virtualadc/580832)
* [利用HTTP Cache来优化网站](https://www.cnblogs.com/cocowool/archive/2011/08/22/2149929.html)
* [很全面的http协议解析](https://blog.csdn.net/MrQkeil/article/details/79577195)
* [让面试官颤抖的 HTTP 2.0 协议面试题](https://blog.csdn.net/zl1zl2zl3/article/details/81901735)
