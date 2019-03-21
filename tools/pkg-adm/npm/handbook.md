# 《npm 手册》 [《MHS 学习笔记》] (mhs2019.3.21)

## 安装
> Nodejs安装(win7)
```
> D:\software\nodejs --- Node安装路径
$ npm c set prefix "F:\Software\npm\global" --- 默认(%AppData%\npm)
$ npm c set cache "F:\Software\npm\cache" --- 默认(%AppData%/npm-cache)
$ set NPM_GLOBAL --- 设置环境变量(F:\Software\npm\global)
> %NPM_GLOBAL% 和 %NPM_GLOBAL%\node_modules --- 添加到环境变量
$ npm add npm -g --- 升级npm
```

## 使用
> npm config
```
npm c delete <key> --- 所有配置文件删除key
npm c edit [-g] --- 打开配置文件，-g全局配置文件
npm c get <key> --- 获取配置值
npm c list [-l] [--json] --- 查看配置，-l默认配置，--json格式
npm c set <key> <value> [-g] --- 设置配置值，-g全局配置
```
> npm help
```
npm help --- 帮助
```
> npm install
```
npm add [<pkg>] [-D] [-g] --- 无包全部安装，-D开发依赖项,-g全局安装
```
> npm ls
```
npm ls [-g] [--depth=0] --- 显示安装列表，-g全局，--depth深度
```
> npm-update
```
npm up [<pkg>] [-g] --- 无包全部安装，-g全局升级
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"

[《npm 手册》]: https://mhsnet.github.io/mhsstudynotes/tools/pkg-adm/npm/handbook.html "《npm 手册》"