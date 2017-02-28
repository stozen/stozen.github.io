# Node.js:事件/代理 <small>Event / Proxy</small>

<ol class="breadcrumb"><li><a href="/">Home</a></li><li><a href="/server/nodejs/overview.md">Node.js</a></li><li class="active">Event/Proxy</li></ol>

### 事件
|名称|网址|说明|
|------|------|------|
|EventProxy|https://github.com/JacksonTian/eventproxy|eventProxy是一款非常好用的javascript事件管理系统，他可以用于前端或者后端|
|Async|https://github.com/caolan/async|当你需要去多个源(一般是小于 10 个)汇总数据的时候，用 eventproxy 方便；当你需要用到队列，需要控制并发数，或者你喜欢函数式编程思维时，使用 async|
|sendevent|https://github.com/fgnass/sendevent|Middleware to stream server-sent events to the client. Browsers that don't support the EventSource interface will fall back to a hidden iframe|

### 回调
|名称|网址|说明|
|------|------|------|
|promise|https://github.com/then/promise|回调函数真正的问题在于他剥夺了我们使用 return 和 throw 这些关键字的能力。而 Promise 很好地解决了这一切|
|Generator|https://github.com/tj/co|Generator是为JavaScript设计的一种轻量级的协程。它通过yield关键字，可以控制一个函数暂停或者继续执行Generator函数有一个特别的语法function* ()，借助这种超能力，我们还可以暂停或者继续执行异步操作，使用像promise或者”thunks”这样的结构来写出看起来像同步的代码|
|nimble|http://caolan.github.io/nimble/|Functional flow-control for JavaScript, that is lightweight and portable. Runs on Node.js and cross-browser, providing a small set of powerful tools, supporting sync and async JavaScript. Combines the most useful features of the underscore and async libraries with a simple API and a vastly reduced filesize|

### 定时任务
|名称|网址|说明|
|------|------|------|
|Node Schedule|https://github.com/node-schedule/node-schedule|node-schedule 是 Node.js 上一个类似 crontab 的定时任务模块|
|Agenda|https://github.com/rschmukler/agenda|Agenda is a light-weight job scheduling library for Node.js|

