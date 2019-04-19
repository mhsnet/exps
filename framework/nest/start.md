# [《MHS 学习笔记》] > [《Nest 学习》] > 开始 (mhs2019.4.9)

- [安装]
- [控制器]
  1. [路由]
  2. [资源]
  3. [路由通配符]
  4. [状态码]
  5. [Headers]
  6. [路由参数]
  7. [请求负载]
- [提供者]
- [模块]
  1. [功能模块]
- [中间件]


## <span id="install">安装</span>
```
node -v  --- node版本>= 8.9.0
npm add @nestjs/cli -g --- 安装Nest CLI
npm run start
```

## <span id="controllers">控制器</span>
> 1. 控制器（使用装饰器创建） --- 接收处理请求
> 2. 路由 --- 控制哪个控制器接收哪些请求

### <span id="controllers-routing">路由</span>
> 1. 路由注册顺序 --- 执行匹配第1个
> 2. @Controller('test') --- 定义路径前缀
> 3. @Get('hello')... --- 定义路径|设置参数
> 4. 默认200，post-201, 自定义@HttpCode(200)
> 5. 返回自动序列化Object|Array->JSON, String->String

### <span id="controllers-resources">资源</span>
> 1. Get|Post|Put|Delete|Patch|Options|Head|All
> 2. @Get()|@Post()|@Put()|@Delete()|@Patch()|@Options()|@Head()|@All()

### <span id="controllers-route-wildcards">路由通配符</span>
> 1. ?,+,*,() --- {0, 1},{1, },通配符(任意字符路径组合),([a-z]?)子表达式

### <span id="controllers-status-code">状态码</span>
> 1. 默认200，post-201
> 2. @HttpCode()自定义
> 3. @Res()注入
> 4. 错误时抛出异常

### <span id="controllers-headers">Headers</span>
> 1. @header() 
> 2. res.header()

### <span id="controllers-route-parameters">路由参数</span>
> 1. GET等 --- @Get()等配置参数|@Param()获取数据
> 2. DTO(数据传输对象)  ---  使用简单类(非接口)
```
//user-test.dto.ts
export default class UserTestDto {
  readonly name: string;
  readonly age: number;
}
//test.controller.ts
//路由参数
@Get('/param/:name/:age')
getParam(@Param() userTestDto: UserTestDto): UserTestDto {
  return userTestDto;
}
```

### <span id="controllers-request-payloads">请求负载</span>
> 1. Post --- @Body()获取数据
> 2. DTO(数据传输对象)  ---  使用简单类(非接口)
```
//user-test.dto.ts
export default class UserTestDto {
  readonly name: string;
  readonly age: number;
}
//test.controller.ts
//Content-Type设置为application/x-www-form-urlencoded
@Post('/param')
postParam(@Body() userTestDto: UserTestDto): UserTestDto {
  return userTestDto;
}
```

## <span id="providers">提供者</span>
> 1. 许多基础类(services,repositories,factories,helpers...)都认为是提供者
> 2. providers只是用@Injectable()注释的类
> 3. 可通过constructor注入依赖关系

## <span id="modules">模块</span>
> 1. 模块是用@Module()的类
> 2. @Module()提供原数据来组织应用结构
> 3. 应用至少1个根模块，模块组织组件，封装相关功能

### <span id="modules-feature-modules">功能模块</span>
> 1. 功能模块 --- 保持代码有序，边界清晰，使用SOLID原则，控制复制性
> 2. CatsController和CatsService属同一应用，密切相关，移入功能模块

## <span id="middleware">中间件</span>
> 1. 路由处理前调用|访问请求|返回对象|
> 2. @Module()提供原数据来组织应用结构
> 3. 应用至少1个根模块，模块组织组件，封装相关功能

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Nest 学习》]: https://mhsnet.github.io/mhsstudynotes/framework/nest/index.html "《Nest 学习》"

[开始]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html "开始"
[安装]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#install "安装"

[控制器]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#controllers "控制器"
[路由]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#controllers-routing "路由"
[资源]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#controllers-resources "资源"
[路由通配符]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#controllers-route-wildcards "路由通配符"
[状态码]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#controllers-status-code "状态码"
[Headers]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#controllers-headers "Headers"
[路由参数]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#controllers-route-parameters "路由参数"
[请求负载]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#controllers-request-payloads "请求负载"

[提供者]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#providers "提供者"

[模块]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#modules "模块"
[功能模块]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#modules-feature-modules "功能模块"

[中间件]: https://mhsnet.github.io/mhsstudynotes/framework/nest/start.html#middleware "中间件"

