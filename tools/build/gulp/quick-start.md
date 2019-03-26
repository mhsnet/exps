# [《MHS 学习笔记》] > [《Gulp 笔记》] > [快速开始] (mhs2019.3.26)

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
$ gulp -h
$ gulp -v
```
## <span id="test">测试</span>
> 新建gulpfile.js
```
function defaultTask(cb) {
  // 默认任务代码放这
  console.log('hello')
  cb();
}

exports.default = defaultTask
```
> 测试
```
$ gulp
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Gulp 笔记》]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/index.html "《Gulp 笔记》"
[快速开始]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/quick-start.html "快速开始"

[安装gulp命令行程序]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/quick-start.html#install "安装gulp命令行程序"
[安装gulp包]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/quick-start.html#install-gulp "安装gulp包"
[测试]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/quick-start.html#test "测试"