# 架构:远程过程调用协议 <small>RPC</small>

<ol class="breadcrumb"><li><a href="/">Home</a></li><li class="active">Architecture</li><li class="active">RPC</li></ol>

## RPC
|名称|网址|说明|
|------|------|------|
|Thrift|https://thrift.apache.org/|thrift是一个软件框架，用来进行可扩展且跨语言的服务的开发。它结合了功能强大的软件堆栈和代码生成引擎，以构建在 C++, Java, Python, PHP, Ruby, Erlang, Perl, Haskell, C#, Cocoa, JavaScript, Node.js, Smalltalk, and OCaml 这些编程语言间无缝结合的、高效的服务|
|Avro|https://avro.apache.org/|Avro是Hadoop中的一个子项目，也是Apache中一个独立的项目，Avro是一个基于二进制数据传输高性能的中间件。在Hadoop的其他项目中例如HBase(Ref)和Hive(Ref)的Client端与服务端的数据传输也采用了这个工具。Avro是一个数据序列化的系统。Avro 可以将数据结构或对象转化成便于存储或传输的格式。Avro设计之初就用来支持数据密集型应用，适合于远程或本地大规模数据的存储和交换|
|ZeroC ICE|https://zeroc.com/products/ice/|ICE是ZEROC的开源通信协议产品，它的全称是：The Internet Communications Engine，翻译为中文是互联网通信引擎，是一个面向对象的中间件，使我们能够以最小的代价构建分布式应用程序。ICE使我们专注于应用逻辑的开发，它来处理所有底层的网络接口编程，这样我们就不用去考虑这样的细节：打开网络连接、网络数据传输的序列化与反序列化、连接失败的尝试次数等|
|Hessian|http://hessian.caucho.com/|Hessian是一个轻量级的remoting onhttp工具，使用简单的方法提供了RMI的功能。 相比WebService，Hessian更简单、快捷。采用的是二进制RPC协议，因为采用的是二进制协议，所以它很适合于发送二进制数据|
|gRPC|https://github.com/grpc/grpc|gRPC是一个高性能、通用的开源RPC框架，其由Google主要面向移动应用开发并基于HTTP/2协议标准而设计，基于ProtoBuf(Protocol Buffers)序列化协议开发，且支持众多开发语言。gRPC提供了一种简单的方法来精确地定义服务和为iOS、Android和后台支持服务自动生成可靠性很强的客户端功能库。客户端充分利用高级流和链接功能，从而有助于节省带宽、降低的TCP链接次数、节省CPU使用、和电池寿命|
|Dubbo|https://github.com/alibaba/dubbo|Dubbo 是阿里巴巴公司开源的一个高性能优秀的服务框架，使得应用可通过高性能的 RPC 实现服务的输出和输入功能，可以和 Spring框架无缝集成|

