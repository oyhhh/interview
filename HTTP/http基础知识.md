什么是HTTP?
  http是超文本传输协议:两点之间传输超文本数据的约定和规范
常见状态码:
  1**:提示信息,协议处理中
  2**:成功
  3**:重定向
  4**:客户端错误
  5**:服务端错误
http常见字段:
  HOST:客户端发送请求时,用来指定服务器的域名
  content-length:本次回应的数据长度
  connection:Keep-alice;TCP长久链接
  content-type:数据格式
  content-encoding:数据的压缩方法
get和post的差别:
  1.get产生一个TCP数据包,浏览器把header和data一起发送,服务端响应200
    POST产生两个TCP数据包,先发header,服务端响应100 continue,浏览器再发送data,然后返回200
  2.get浏览器主动cache ,post不会
  3.get传参有长度限制 ie和safari都是2k,opera是4k,firefox是8k,post没有
  4.get通过url传参,post通过body
无状态协议:浏览器对于事务的处理没有记忆能力
JWT(Json web token):cookie存在客户端,支持跨域认证

TCP 和 UDP
 TCP 是面向连接的协议 。 UDP 是无连接的协议
 TCP 在发送数据前先需要建立连接，然后再发送数据 。 UDP 无需建立连接就可以直接发送大量数据
 TCP 会按照特定顺序重新排列数据包 。 UDP 数据包没有固定顺序，所有数据包都相互独立
 TCP 传输的速度比较慢 。 UDP 的传输会更快
 TCP 的头部字节有 20 字节 。 UDP 的头部字节只需要 8 个字节
 TCP 是重量级的，在发送任何用户数据之前，TCP需要三次握手建立连接。 UDP 是轻量级的。没有跟踪连接，消息排序等。
 TCP 会进行错误校验，并能够进行错误恢复 。 UDP 也会错误检查，但会丢弃错误的数据包。
 TCP 有发送确认。 UDP 没有发送确认
 TCP 会使用握手协议，例如 SYN(同步序列编号)，SYN-ACK，ACK(确认字符)。 UDP无握手协议
 TCP 是可靠的，因为它可以确保将数据传送到路由器。 UDP 中不能保证将数据传送到目标。
 
 
 输入内容浏览器经历了什么?
   URL地址->去本地找是否有DNS缓存->有返回IP
                               ->没有网络查询DNS     在由根域名服务器 -> 顶级域名服务器 -> 权威 DNS 服务器后，由权威服务器告诉本地服务器目标 IP 地址，再有本地 DNS 服务器告诉用户需要访问的 IP 地址。
                               
                               浏览器和目标服务器简历TCP连接
