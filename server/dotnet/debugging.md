# <span class="fa fa-windows" aria-hidden="true"></span> .Net:调试 <small>Debugging</small>

<ol class="breadcrumb"><li><a href="/">Home</a></li><li><a href="/server/dotnet/overview.md">.Net</a></li><li class="active">Debugging</li></ol>

### 路由调试
|名称|网址|说明|
|------|------|------|
|RouteDebugger|http://www.nuget.org/packages/routedebugger|在Asp.Net MVC程序中，路由(Route)是一个非常核心的概念，可以说是MVC程序的入口，因为每一个Http请求都要经过路由计算，然后匹配到相应的Controller和Action。通常我们的路由都会注册在Global.asax.cs文件中的RegisterRoutes方法中，路由会从上往下依次匹配，因此自定义的（优先级高）的路由需要放在默认（通用）路由的前面。但是，如何确保所有的路由都是正确的，或者是没有重复的呢？RouteDebug 与 RouteDebugger就是这样一个分析工具|

