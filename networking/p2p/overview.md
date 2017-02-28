# <span class="fa fa-globe" aria-hidden="true"></span> 网络:对等网络 <small>P2P</small>

<ol class="breadcrumb"><li><a href="/">Home</a></li><li class="active">P2P</li></ol>

### 有中心组网

### 无中心自组网

### 分布式哈希表(DHT)
DHT(Distributed Hash Table，分布式哈希表)类似Tracker的根据种子特征码返回种子信息的网络。DHT全称叫分布式哈希表(Distributed Hash Table)，是一种分布式存储方法。在不需要服务器的情况下，每个客户端负责一个小范围的路由，并负责存储一小部分数据，从而实现整个DHT网络的寻址和存储。新版BitComet允许同行连接DHT网络和Tracker，也就是说在完全不连上Tracker服务器的情况下，也可以很好的下载，因为它可以在DHT网络中寻找下载同一文件的其他用户

### 基于命名数据组网(NDN)
NDN从UC-Berkeley的Scott Shenker教授等提出的DONA体系结构出发，它采用名字路由，通过路由器来缓存内容，从而使数据传输更快，并能提高内容的检索效率。NDN的具体实现例子是施乐公司的帕洛阿托研究中心（PARC）的Van Jacobson等提出的内容中心网络，简称CCN（Content-Centric Networking）

