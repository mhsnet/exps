# install [《MHS 学习笔记》] -> [《npm CLI》] (mhs2019.3.7)

```
$ npm install (with no args, in package dir) --- 本地node_modules安装项目依赖
> -g --- 当前目录安装为全局
> --production --- [或NODE_ENV设为production]不安装devDependencies
$ npm install [<@scope>/]<name>
$ -g --- 命令后-g全局安装
$ -P --- [Default] 添加到dependencies
$ -D --- 添加到devDependencies
$ npm install [<@scope>/]<name>@<tag>
$ npm install [<@scope>/]<name>@<version>
$ npm install [<@scope>/]<name>@<version range>
$ npm install <git-host>:<git-user>/<repo-name>
$ npm install <git repo url>
$ npm install <tarball file>
$ npm install <tarball url>
$ npm install <folder>

$ aliases: npm i, npm add
$ common options: [-P|--save-prod|-D|--save-dev|-O|--save-optional] [-E|--save-exact] [-B|--save-bundle] [--no-save] [--dry-run]
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《npm CLI》]: https://mhsnet.github.io/mhsstudynotes/tools/npm/cli/index.html "《npm CLI》"

[install]: https://mhsnet.github.io/mhsstudynotes/tools/npm/cli/cli/install.html "install"