<details>
<summary>常用的HTTP方法有哪些？</summary>

GET： 用于请求访问已经被URI（统一资源标识符）识别的资源，可以通过URL传参给服务器

POST：用于传输信息给服务器，主要功能与GET方法类似，但一般推荐使用POST方式。

PUT： 传输文件，报文主体中包含文件内容，保存到对应URI位置。

HEAD： 获得报文首部，与GET方法类似，只是不返回报文主体，一般用于验证URI是否有效。

DELETE：删除文件，与PUT方法相反，删除对应URI位置的文件。

OPTIONS：查询相应URI支持的HTTP方法。

</details>

<details>
<summary>GET方法与POST方法的区别</summary>

[程序员：我终于知道post和get的区别](https://www.jianshu.com/p/2e2c064f1a8b)

[为什么请求时,需要使用URLEncode做encode转码操作](https://blog.csdn.net/u013833031/article/details/78828539)


区别一：

get重点在从服务器上获取资源，post重点在向服务器发送数据；

区别二：

get传输数据是通过URL请求，以field（字段）= value的形式，置于URL后，并用"?"连接，多个请求数据间用"&"连接，如http://127.0.0.1/Test/login.action?name=admin&password=admin，这个过程用户是可见的；

post传输数据通过Http的post机制，将字段与对应值封存在请求实体中发送给服务器，这个过程对用户是不可见的；

区别三：

Get传输的数据量小，因为受URL长度限制，但效率较高；

Post可以传输大量数据，所以上传文件时只能用Post方式；

区别四：

get是不安全的，因为URL是可见的，可能会泄露私密信息，如密码等；

post较get安全性较高；

区别五：

get方式只能支持ASCII字符，向服务器传的中文字符可能会乱码。

post支持标准字符集，可以正确传递中文字符。

</details>

<details>
<summary>HTTP请求报文与响应报文格式</summary>

请求报文包含三部分：

a、请求行：包含请求方法、URI、HTTP版本信息

b、请求首部字段

c、请求内容实体

响应报文包含三部分：

a、状态行：包含HTTP版本、状态码、状态码的原因短语

b、响应首部字段

c、响应内容实体

</details>

<details>
<summary>常见的HTTP相应状态码</summary>

200：请求被正常处理

204：请求被受理但没有资源可以返回

206：客户端只是请求资源的一部分，服务器只对请求的部分资源执行GET方法，相应报文中通过Content-Range指定范围的资源。

301：永久性重定向

302：临时重定向

303：与302状态码有相似功能，只是它希望客户端在请求一个URI的时候，能通过GET方法重定向到另一个URI上

304：发送附带条件的请求时，条件不满足时返回，与重定向无关

307：临时重定向，与302类似，只是强制要求使用POST方法

400：请求报文语法有误，服务器无法识别

401：请求需要认证

403：请求的对应资源禁止被访问

404：服务器无法找到对应资源

500：服务器内部错误

503：服务器正忙

</details>

<details>
<summary>HTTP1.1版本新特性</summary>

a、默认持久连接节省通信量，只要客户端服务端任意一端没有明确提出断开TCP连接，就一直保持连接，可以发送多次HTTP请求

b、管线化，客户端可以同时发出多个HTTP请求，而不用一个个等待响应

c、断点续传原理

</details>

<details>
<summary>HTTP必知必会——断点续传原理</summary>

要实现断点续传的功能，通常都需要客户端记录下当前的下载进度，并在需要续传的时候通知服务端本次需要下载的内容片段。

HTTP1.1协议（RFC2616）中定义了断点续传相关的HTTP头 Range和Content-Range字段，一个最简单的断点续传实现大概如下： 

  1.客户端下载一个1024K的文件，已经下载了其中512K 
  
  2. 网络中断，客户端请求续传，因此需要在HTTP头中申明本次需要续传的片段： 
  
    Range:bytes=512000- 
    
    这个头通知服务端从文件的512K位置开始传输文件 
  
  3. 服务端收到断点续传请求，从文件的512K位置开始传输，并且在HTTP头中增加： 
    
     Content-Range:bytes 512000-/1024000 
     
     并且此时服务端返回的HTTP状态码应该是206，而不是200。 

但是在实际场景中，会出现一种情况，即在终端发起续传请求时，URL对应的文件内容在服务端已经发生变化，此时续传的数据肯定是错误的。如何解决这个问题了？显然此时我们需要有一个标识文件唯一性的方法。在RFC2616中也有相应的定义，比如实现Last-Modified来标识文件的最后修改时间，这样即可判断出续传文件时是否已经发生过改动。同时RFC2616中还定义有一个ETag的头，可以使用ETag头来放置文件的唯一标识，比如文件的MD5值。

终端在发起续传请求时应该在HTTP头中申明If-Match 或者If-Modified-Since 字段，帮助服务端判别文件变化。 

另外RFC2616中同时定义有一个If-Range头，终端如果在续传是使用If-Range。If-Range中的内容可以为最初收到的ETag头或者是Last-Modfied中的最后修改时候。服务端在收到续传请求时，通过If-Range中的内容进行校验，校验一致时返回206的续传回应，不一致时服务端则返回200回应，回应的内容为新的文件的全部数据。

[HTTP必知必会——断点续传原理](https://blog.csdn.net/zhangliangzi/article/details/51348755)

[HTTP文件断点续传原理解析(源码)](https://blog.csdn.net/Awenyini/article/details/77898704)

</details>

<details>
<summary>常见HTTP首部字段</summary>

a、通用首部字段（请求报文与响应报文都会使用的首部字段）

  Date：创建报文时间
  
  Connection：连接的管理
  
  Cache-Control：缓存的控制
  
  Transfer-Encoding：报文主体的传输编码方式
b、请求首部字段（请求报文会使用的首部字段）
  
  Host：请求资源所在服务器
  
  Accept：可处理的媒体类型
  
  Accept-Charset：可接收的字符集
  
  Accept-Encoding：可接受的内容编码
  
  Accept-Language：可接受的自然语言
  
c、响应首部字段（响应报文会使用的首部字段）
  
  Accept-Ranges：可接受的字节范围
  
  Location：令客户端重新定向到的URI
  
  Server：HTTP服务器的安装信息
  
d、实体首部字段（请求报文与响应报文的的实体部分使用的首部字段）
  
  Allow：资源可支持的HTTP方法
  
  Content-Type：实体主类的类型
  
  Content-Encoding：实体主体适用的编码方式
  
  Content-Language：实体主体的自然语言
  
  Content-Length：实体主体的的字节数
  
  Content-Range：实体主体的位置范围，一般用于发出部分请求时使用

</details>

<details>
<summary>HTTP的缺点与HTTPS</summary>

a、通信使用明文不加密，内容可能被窃听

b、不验证通信方身份，可能遭到伪装

c、无法验证报文完整性，可能被篡改

HTTPS就是HTTP加上加密处理（一般是SSL安全通信线路）+认证+完整性保护

</details>

<details>
<summary>30 张图解 HTTP 常见的面试题</summary>

* [硬核！30 张图解 HTTP 常见的面试题](https://mp.weixin.qq.com/s/FJGKObVnU61ve_ioejLrtw)

</details>































---
---

<details>
<summary>1. 你怎么理解http协议？</summary>

</details>

<details>
<summary>2. 说说http协议的工作流程</summary>


</details>

<details>
<summary>3. http有哪些请求提交方式？</summary>



</details>

<details>
<summary>4. http中的200,302,403,404,500,503都代表什么状态？</summary>


</details>

<details>
<summary>5.http get和post有什么区别？</summary>


</details>

<details>
<summary> 6. 什么是https，说说https的工作原理？</summary>



</details>

<details>
<summary>7. 什么是http代理服务器，有什么用？</summary>


</details>
