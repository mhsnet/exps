# 开始 [Home] [Aqueduct] (mhs2019.2.21)

- [安装]
- [创建项目]
- [链接控制器]
- [高级路由]
- [资源控制器]
- [多线程和应用程序状态]

## <span id="installation">安装</span> [Top]
```
$ pub global activate aqueduct --- 安装Aqueduct命令行工具
```

## <span id="creating-project">创建项目</span> [Top]
```
$ aqueduct create dart_study_server --- 创建Aqueduct项目
$ aqueduct serve --- 启动项目
```

## <span id="linking-controllers">链接控制器(Linking Controllers)</span> [Top]
```
@override
Controller get entryPoint {
  final router = Router();
  
  router
    .route('/users')
    .link(() => APIKeyValidator())
    .link(() => Authorizer.bearer())
    .link(() => UsersController());

  router
    .route('/posts')
    .link(() => APIKeyValidator())
    .link(() => PostsController());

  return router;
}
```
> 控制器处理请求(request)，可发送响应（response）或让链接控制器处理。默认router发送404，添加（a route）到router，创建控制器可以链接到的新通道(channel)入口点(entry point)。

> 控制器分终点(Endpoint)和中间件(Middleware)：
> 1. 终点控制器(Endpoint controllers)：发送响应(response)，实现请求(request)寻求的行为。
> 2. 中间件控制器(Middleware controllers)：可创建任何中间件，在到达终端控制器前处理请求(request)，提供你喜欢的行为。例（Router：将请求定向到正确的控制器；Authorizer：验证请求的授权）。

> 通道可有0或多个中间件控制器，以终点控制器结束。大多控制器只能有一个链接控制器，但路由可有多个。

## <span id="advanced-routing">高级路由(Advanced Routing)</span> [Top]
> 1. /:xxx --- 路径变量
> 2. /[:xxx] --- 路径变量可选 
```
router
  .route('/users/[:id]')
  .link(() => UsersController());
```

## <span id="resource-controllers">资源控制器(ResourceControllers)</span> [Top]
> 例（lib/controller/users_controller.dart）：
```
import 'package:aqueduct/aqueduct.dart';
import 'package:dart_study_server/dart_study_server.dart';

class UsersController extends ResourceController {
  final _users = [
    {'id': 1, 'name': '用户1'},
    {'id': 2, 'name': '用户2'},
    {'id': 3, 'name': '用户3'}
  ];

  @Operation.get()
  Future<Response> getAllUsers() async {
    return Response.ok(_users);
  }

  @Operation.get('id')
  Future<Response> getUserByID(@Bind.path('id') int id) async {
    final user =
        _users.firstWhere((user) => user['id'] == id, orElse: () => null);
    if (user == null) {
      return Response.notFound();
    }
    return Response.ok(user);
  }
}
```
> 资源控制器(ResourceController)：每个方法都有一个操作注释(Operation annotation)，用于标识请求必须触发的HTTP方法和路径变量。

> 可以绑定路径变量(path variables)、头(headers)、查询参数(query parameters)和主体(bodies)。绑定路径变量时，我们必须用参数指定哪个路径变量为@Bind.path(pathvariablename)

## <span id="multi-threading-and-application-state">多线程和应用程序状态(Multi-threading and Application State)</span> [Top]
> 1. 将数据存数据库，使程序重启时不丢失。
> 2. 伴随部署容器化，无状态Web服务成为一种需求，Aqueduct多线程使检查违反此规则更容易。
> 3. Aqueduct运行时创建多线程，每个线程拥有独立isolated，数据不能访问其它线程。
> 4. 每个isolated创建通道实例，每个请求只提供1个isolated，负载均衡器后多个服务运行行为相同，并且速度更快。
> 5. 应用程序中存储数据，更改数据只会在某个isolated中更改，再次请求不太可能看到更改—另一个具有不同数据的isolated可能处理该请求。

##
[Home]: https://mhsnet.github.io/mhsstudynotes/ "《MHS技术栈学习笔记》"
[Aqueduct]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/index.html "《Aqueduct》"
[Top]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/getting_started.html "开始"

[安装]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/getting_started.html#installation "安装(Installation)"
[创建项目]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/getting_started.html#creating-project "创建项目(Creating a Project)"
[链接控制器]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/getting_started.html#linking-controllers "链接控制器(Linking Controllers)"
[高级路由]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/getting_started.html#advanced-routing "高级路由(Advanced Routing)"
[资源控制器]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/getting_started.html#resource-controllers  "资源控制器(ResourceControllers)"
[多线程和应用程序状态]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/getting_started.html#multi-threading-and-application-state  "多线程和应用程序状态(Multi-threading and Application State)"