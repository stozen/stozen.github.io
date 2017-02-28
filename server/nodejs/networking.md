# Node.js:网络 <small>Networking</small>

<ol class="breadcrumb"><li><a href="/">Home</a></li><li><a href="/server/nodejs/overview.md">Node.js</a></li><li class="active">Networking</li></ol>

### HTTP模块
|名称|网址|说明|
|------|------|------|
|SuperAgent|https://github.com/visionmedia/superagent|SuperAgent 是一个轻量的Ajax API，服务器端（Node.js）客户端（浏览器端）均可使用,SuperAgent具有学习曲线低、使用简单、可读性好的特点,可作为客户端请求代理模块使用，当你想处理get,post,put,delete,head请求时，可以考虑使用SuperAgent|
|cookie-parser|https://github.com/expressjs/cookie-parser|我的理解是，转换headers中的cookie并跟req.cookies合并。作为cookie-parser的核心，parser提示了2个函数：signedCookies和JSONCookies，以及它们的帮助函数|
|body-parser|https://github.com/expressjs/body-parser|bodyParser中间件用来解析http请求体，是express默认使用的中间件之一。使用express应用生成器生成一个网站，它默认已经使用了 bodyParser.json 与 bodyParser.urlencoded 的解析功能，除了这两个，bodyParser还支持对text、raw的解析|

### 邮件模块
|名称|网址|说明|
|------|------|------|
|Nodemailer|https://github.com/nodemailer/nodemailer|Nodemailer 是一个简单易用的 Node.JS 邮件发送模块（通过 SMTP，sendmail，或者 Amazon SES），支持 unicode，你可以使用任何你喜欢的字符集|

### Socket模块
|名称|网址|说明|
|------|------|------|
|socket.io|https://github.com/socketio/socket.io|Socket.IO 实现了实时双向的基于事件的通讯机制。旨在让各种浏览器与移动设备上实现实时app功能，模糊化各种传输机制。Socket.IO 是跨平台，多种连接方式自动切换，做即时通讯方面的开发很方便，而且能和expressjs提供的传统请求方式很好的结合，即可以 在同一个域名，同一个端口提供两种连接方式：request/response, websocket(flashsocket,ajax…)|


### 网络常用模块
|名称|网址|说明|
|------|------|------|
|net-ping|https://github.com/stephenwvickers/node-net-ping|net-ping- node.js 对ping的封装，用于测试目标主机是否可达|

