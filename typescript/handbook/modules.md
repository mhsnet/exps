# [《MHS 学习笔记》] > [《TypeScript 手册》] > [模块] (mhs2019.3.28)

- [安装gulp命令行程序]
- [安装gulp包]
- [测试]

## <span id="install">安装gulp命令行程序</span>
```
$ node -v
$ npm -v
$ npx -v
$ npm ls --depth=0 -g
$ npm add gulp-cli -g
```
## <span id="install-gulp">安装gulp包</span>
```
$ npx mkdirp my-dir --- 目录www_test/gulp
$ cd my-dir
$ npm init -y
$ npm add gulp -D
$ npm add ts-node -D
$ npm add typescript -D
$ gulp -h
$ gulp -v
```
## <span id="test">测试</span>
> 新建gulpfile.ts/index.ts
```
function taskA(cb) {
  console.log('Hello Task A');
  cb();
};

function taskB(cb) {
  console.log('Hello Task B');
  cb();
};

export { taskA as default, taskB };
```
> 测试
```
$ gulp
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《TypeScript 手册》]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/index.html "《TypeScript 手册》"
[模块]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/modules.html "模块"