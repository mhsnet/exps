# 《yarn 手册》 [《MHS 学习笔记》] (mhs2019.3.21)

## 安装
> Yarn安装(win7)
```
> D:\software\Yarn --- Yarn安装路径
$ yarn config set global-folder "F:\Software\yarn\global" --- 默认(%AppData%\npm)
$ yarn config set cache-folder "F:\Software\yarn\cache" --- 默认(%AppData%/npm-cache)
$ set YARN_GLOBAL --- 设置环境变量(F:\Software\yarn\global)
> %YARN_GLOBAL%\node_modules\.bin --- 添加到环境变量
$ yarn global bin --- bin路径
$ yarn global dir --- 安装位置
$ yarn add nrm --- 安装资源管理软件
$ nrm use taobao --- 使用淘宝源
```

## 使用
> yarn add --- 安装
```
yarn add [<pkg>] [-D] --- 无包名全部安装，-D开发依赖项
```
> yarn config --- 配置
```
yarn config delete <key> --- 所有配置文件删除key
yarn config get <key> --- 获取配置值
yarn config list [-l] [--json] --- 查看配置，-l默认配置，--json格式
yarn config set <key> <value> [-g] --- 设置配置值，-g全局配置
```
> yarn global --- 全局操作
``` 
yarn global <add/bin/list/remove/upgrade> [--prefix]
```
> yarn help --- 帮助
```
yarn help
```
> yarn list --- 显示已安装包列表
```
yarn list [--depth=0] --- --depth深度
```
> yarn remove --- 删除包
```
yarn remove [<pkg>] 
```
> yarn upgrade --- 更新包
```
yarn upgrade [<pkg>] --- 无包名全部安装
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"

[《yarn 手册》]: https://mhsnet.github.io/mhsstudynotes/tools/pkg-adm/yarn/handbook.html "《yarn 手册》"