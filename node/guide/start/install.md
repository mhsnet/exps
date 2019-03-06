# 安装 [《MHS 学习笔记》] -> [《Node 指南》] (mhs2019.2.28)

- [安装win7]
- [安装CentOS7]

## <span id="install-win7">安装win7</span> [安装]
> 安装：
> ```
> $e node-v10.15.1-x64.msi  --- 启动nodejs安装程序
> $e D:\\software\\nodejs --- 设置路径
> $ npm install npm@latest -g --- npm 升级
> $ npm config set registry https://registry.npm.taobao.org --- 配置源(https://registry.npmjs.org/)
> ```

> 升级：
> 1. 卸载
> 2. 重新安装

## <span id="install-centos7">安装CentOS7</span> [安装]
> 安装：
> 添加nodejs的YUM源
> ```
> $ yum install -y nodejs
> $ npm install npm@latest -g --- npm 升级
> $ npm config set registry https://registry.npm.taobao.org --- 配置源(https://registry.npmjs.org/)
> ```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Node 指南》]: https://mhsnet.github.io/mhsstudynotes/node/guide/index.html "《Node 指南》"
[安装]: https://mhsnet.github.io/mhsstudynotes/node/guide/start/install.html "安装"

[安装win7]: https://mhsnet.github.io/mhsstudynotes/node/guide/start/install.html#install-win7 "安装win7"
[安装CentOS7]: https://mhsnet.github.io/mhsstudynotes/node/guide/start/install.html#install-centos7 "安装CentOS7"