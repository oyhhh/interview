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
http的优点和缺点以及性能:
 
 
