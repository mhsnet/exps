# [《MHS 学习笔记》] > [《Nest 学习》] > 技术 (mhs2019.4.12)

- [验证]
  1. [安装]
- [热重载]
  1. [安装]
  2. [配置]
  3. [热模块替换]

## <span id="auth">验证</span>
> 1. Passport验证库

### <span id="auth-install">1. 安装</span>
```
$ npm add @nestjs/passport passport passport-http-bearer
```

## <span id="hot-reload">热重载</span>
> 1. webpack HMR (Hot-Module Replacement)

### <span id="hot-reload-installation">1. 安装</span>
```
$ npm add webpack webpack-cli webpack-node-externals ts-loader -D
```

### <span id="hot-reload-configuration">2. 配置</span>
> 根目录添加webpack.config.js
```
const webpack = require('webpack');
const path = require('path');
const nodeExternals = require('webpack-node-externals');

module.exports = {
  entry: ['webpack/hot/poll?100', './src/main.ts'],
  watch: true,
  target: 'node',
  externals: [
    nodeExternals({
      whitelist: ['webpack/hot/poll?100'],
    }),
  ],
  module: {
    rules: [
      {
        test: /.tsx?$/,
        use: 'ts-loader',
        exclude: /node_modules/,
      },
    ],
  },
  mode: 'development',
  resolve: {
    extensions: ['.tsx', '.ts', '.js'],
  },
  plugins: [new webpack.HotModuleReplacementPlugin()],
  output: {
    path: path.join(__dirname, 'dist'),
    filename: 'app.js',
  },
};
```

### <span id="hot-reload-configuration">3. 热模块替换</span>
> 应用入口改写(main.ts)
```
import { NestFactory } from '@nestjs/core';
import { AppModule } from './app.module';

declare const module: any;

async function bootstrap() {
  const app = await NestFactory.create(AppModule);
  await app.listen(3000);

  if (module.hot) {
    module.hot.accept();
    module.hot.dispose(() => app.close());
  }
}
bootstrap();
```
> package.json
```
"start": "node dist/app",
"webpack": "webpack --config webpack.config.js"
```
```
npm run webpack
npm run start
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Nest 学习》]: https://mhsnet.github.io/mhsstudynotes/framework/nest/index.html "《Nest 学习》"

[技术]: https://mhsnet.github.io/mhsstudynotes/framework/nest/techniques.html "技术"

[验证]: https://mhsnet.github.io/mhsstudynotes/framework/nest/techniques.html#auth "验证"
[安装]: https://mhsnet.github.io/mhsstudynotes/framework/nest/techniques.html#auth-install "安装"

[热重载]: https://mhsnet.github.io/mhsstudynotes/framework/nest/techniques.html#hot-reload "热重载"
[安装]: https://mhsnet.github.io/mhsstudynotes/framework/nest/techniques.html#hot-reload-installation "安装"
[配置]: https://mhsnet.github.io/mhsstudynotes/framework/nest/techniques.html#hot-reload-configuration "配置"
[热模块替换]: https://mhsnet.github.io/mhsstudynotes/framework/nest/techniques.html#hot-reload-hot-module-replacement "热模块替换"