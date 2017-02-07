# 架构:负载均衡 <small>Load Balance</small>

<ol class="breadcrumb"><li><a href="/">Home</a></li><li class="active">Architecture</li><li class="active">Load Balance</li></ol>

## Http负载均衡
|名称|网址|说明|
|------|------|------|
|Nginx|http://nginx.org/|Nginx不仅是一个小巧且高效的HTTP服务器，也可以做一个高效的负载均衡反向代理，通过它接受用户的请求并分发到多个Mongrel进程可以极大提高Rails应用的并发能力|

## Tcp负载均衡
|名称|网址|说明|
|------|------|------|
|LVS|https://github.com/alibaba/LVS|LVS(LinuxVirtual Server)是由章文嵩博士主导开发的一款开源软件，可以实现Linux平台下的基于网络层的负载均衡软件|
|Keepalived|https://github.com/acassen/keepalived|Keepalived的作用是检测服务器的状态，如果有一台web服务器死机，或工作出现故障，Keepalived将检测到，并将有故障的服务器从系统中剔除，当服务器工作正常后Keepalived自动将服务器加入到服务器群中，这些工作全部自动完成，不需要人工干涉，需要人工做的只是修复故障的服务器|
|HAProxy|http://www.haproxy.com/|HAProxy提供高可用性、负载均衡以及基于TCP和HTTP应用的代理，支持虚拟主机，它是免费、快速并且可靠的一种解决方案。HAProxy特别适用于那些负载特大的web站点，这些站点通常又需要会话保持或七层处理。HAProxy运行在当前的硬件上，完全可以支持数以万计的并发连接。并且它的运行模式使得它可以很简单安全的整合进您当前的架构中， 同时可以保护你的web服务器不被暴露到网络上|

