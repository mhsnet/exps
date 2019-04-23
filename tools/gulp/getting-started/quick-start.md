# [《MHS 学习笔记》] > [《Gulp 学习》] > [开始] (mhs2019.4.23)

- [检查node|npm|npx]
- [安装gulp包]
- [使用库]
- [测试]

## <span id="check-for-node-npm-and-npx">检查node|npm|npx</span>
```
$ node -v
$ npm -v
$ npx -v
```

## <span id="install-gulp">安装gulp包</span>
> 1. 支持Typescript
```
$ npm ls --depth=0 -g
$ npm add gulp-cli -gnpm add ts-node -D
$ npx mkdirp tp-gts --- 目录tp-gts
$ cd tp-gts
$ npm init -y
$ npm add @types/gulp -D
$ npm add gulp -D
$ npm add ts-node -D
$ npm add typescript -D
```

## <span id="use-lib">使用库</span>
```
$ npm add lodash -D
$ npm add @types/lodash -D
```

## <span id="test">测试</span>
> 测试代码
```
// tp-gts/gulpfile.ts/index.ts
import * as _ from 'lodash'

function taskTest(cb) {
  let str = 'hello typescript gulp!';
  str = _.capitalize(str);
  console.log(`${str}`);
  cb();
};

export { taskTest as default };
```
> 测试
```
$ gulp
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Gulp 学习》]: https://mhsnet.github.io/mhsstudynotes/tools/gulp/index.html "《Gulp 学习》"

[《开始》]: https://mhsnet.github.io/mhsstudynotes/tools/gulp/getting-started/quick-start.html "《开始》"

[检查node|npm|npx]: https://mhsnet.github.io/mhsstudynotes/tools/gulp/getting-started/quick-start.html#check-for-node-npm-and-npx "检查node|npm|npx"
[安装gulp包]: https://mhsnet.github.io/mhsstudynotes/tools/gulp/getting-started/quick-start.html#install-gulp "安装gulp包"
[使用库]: https://mhsnet.github.io/mhsstudynotes/tools/gulp/getting-started/quick-start.html#use-lib "使用库"
[测试]: https://mhsnet.github.io/mhsstudynotes/tools/gulp/getting-started/quick-start.html#test "测试"