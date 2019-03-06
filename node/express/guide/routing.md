# 路由 [《MHS 学习笔记》] -> [《Express 学习》] (mhs2019.3.4)

- [路由方法]
- [路由路径]
- [Route参数]
- [Route处理]
- [Response方法]
- [app.route()]
- [express.Router]

## <span id="route-methods">路由方法</span> [路由]
> Express支持所有HTTP请求方法(get,post,put,delete...)。
```
app.[get|post|put|delete]('/', function (req, res) {
  res.send('get|post|put|delete')
})
```

## <span id="route-paths">路由路径</span> [路由]
```
app.get('/', function (req, res) {
  res.send('root')
})

```

## <span id="route-parameters">Route参数</span> [路由]
```
app.get('/', function (req, res) {
  res.send('root')
})

```

## <span id="route-handlers">Route处理</span> [路由]
> 可提供多个回调，类似中间件除了可能调用next(“route”)来绕过剩余回调
```
let cb0 = function timeLog(req, res, next) {
  const myDate = new Date();
  console.log(`时间(${myDate.toLocaleString()})`)
  next()
}

let cb1 = function (req, res) {
  res.send('Hello Get')
}

let cb2 = function (req, res) {
  res.send('Hello Post')
}
...
// 返回单个路由实例，进行HTTP链式操作
router.route('/hello')
  .all([cb0])
  .get([cb1])
  .post([cb2])
```

## <span id="response-methods">Response方法</span> [路由]

## <span id="app-route">app.route()</span> [路由]
> app.route()返回单个路由实例，进行HTTP链式操作
```
// 返回单个路由实例，进行HTTP链式操作
router.route('/hello')
  .all(function timeLog(req, res, next) {
    const myDate = new Date();
    console.log(`时间(${myDate.toLocaleString()})`)
    next()
  })
  .get(function (req, res) {
    res.send('Hello Get')
  })
  .post(function (req, res) {
    res.send('Hello Post')
  })
```

## <span id="express-router">express.Router</span> [路由]
> express.Router(Class)创建模块化，可安装的路由程序(Instance) ，包含完整中间件和路由系统(mini_app)。
```
// 迷你应用（test）
const express = require('express')
const router = express.Router()

// 使用中间件
router.use(function timeLog (req, res, next) {
  const myDate = new Date();
  console.log(`时间(${myDate.toLocaleString()})`)
  next()
})
// 定义首页
router.get('/', function (req, res) {
  res.send('迷你应用Test首页')
})

module.exports = router
```
```
const mini_app_test = require('./mini_apps/test')
const express = require('express')
const app = express()
const port = 3000

app.use('/test', mini_app_test)

app.listen(port, () => console.log(`应用程序监听端口（${port}）`))
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/note/ "《MHS 学习笔记》"
[《Express 学习》]: https://mhsnet.github.io/note/node/express/index.html "《Express 学习》"

[路由]: https://mhsnet.github.io/note/node/express/guide/routing.html "路由"
[路由方法]: https://mhsnet.github.io/note/node/express/guide/routing.html#route-methods "路由方法"

[路由路径]: https://mhsnet.github.io/note/node/express/guide/routing.html#route-paths "路由路径"
[Route参数]: https://mhsnet.github.io/note/node/express/guide/routing.html#route-parameters "Route参数"
[Route处理]: https://mhsnet.github.io/note/node/express/guide/routing.html#route-handlers "Route处理"
[Response方法]: https://mhsnet.github.io/note/node/express/guide/routing.html#response-methods "Response方法"
[app.route()]: https://mhsnet.github.io/note/node/express/guide/routing.html#app-route "app.route()"
[express.Router]: https://mhsnet.github.io/note/node/express/guide/routing.html#express-router "express.Router"