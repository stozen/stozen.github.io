# Java:日志 <small>Logging</small>

<ol class="breadcrumb"><li><a href="/">Home</a></li><li><a href="/java/overview.md">Java</a></li><li class="active">Logging</li></ol>

## 日志库
|名称|网址|说明|
|------|------|------|
|log4j|https://github.com/apache/log4j/|Log4j是一款基于Java的开源日志组件，Log4j功能非常强大，我们可以将日志信息输出到控制台、文件、用户界面，也可以输出到操作系统的事件记录器和一些系统常驻进程。更值得一提的是，Log4j可以允许你非常便捷地自定义日志格式和日志等级，可以帮助开发人员全方位地掌控日志信息|
|Logback|https://github.com/qos-ch/logback/|Logback是由log4j创始人设计的又一个开源日志组件。logback当前分成三个模块：logback-core,logback- classic和logback-access。logback-core是其它两个模块的基础模块。logback-classic是log4j的一个 改良版本。此外logback-classic完整实现SLF4J API使你可以很方便地更换成其它日志系统如log4j或JDK14 Logging。logback-access访问模块与Servlet容器集成提供通过Http来访问日志的功能|
|commons-logging|http://commons.apache.org/proper/commons-logging/|Commons Logging (JCL)提供的是一个日志(Log)接口(interface)，同时兼顾轻量级和不依赖于具体的日志实现工具。它提供给中间件/日志工具开发者一个简单的日志操作抽象，允许程序开发人员使用不同的具体日志实现工具|

## 日志查看工具
|名称|网址|说明|
|------|------|------|
|gclogviewer|http://code.google.com/p/gclogviewer/|gclogviewer是一个支持jdk 6的gc log可视化工具，和gcviewer相比，gclogviewer支持根据gc log生成GC的趋势图，也支持生成调优建议所需的数据趋势图|

## 日志转换工具
|名称|网址|说明|
|------|------|------|
|SLF4J|https://github.com/qos-ch/slf4j/|SLF4J提供了一个简单统一的日志记录接口，开发者在配置和部署时只需要实现这个接口即可实现日志功能。 Logging API实现既可以选择直接实现SLF4J接的loging APIs如： NLOG4J、SimpleLogger。也可以通过SLF4J提供的API实现来开发相应的适配器如Log4jLoggerAdapter、JDK14LoggerAdapter|

