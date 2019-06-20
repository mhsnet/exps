# [《MHS 学习笔记》] > [《VSCode 插件开发》] (mhs2019.5.10)

- 开始
  1. [第一个扩展]

## 开始
### <span id="get-start-first-extension">1. 第一个扩展</span>
> 安装Yeoman和VS Code Extension Generator，创建第一个扩展
```
$ npm add -g yo generator-code
$ yo code
> cd std
> New Extension(TypeScript)
> vsctest
$ cd vsctest
$ F5 --- 调试(扩展调试)
$ ⇧⌘P --- 命令面板
$ Hello Word --- 提示(Hello Word)
```
> 开发扩展(小修改)
> 1. 改变信息
> 2. ⌘R(Developer: Reload Window)
> 3. 重新Hello World
```
// src/extension.ts
//vscode.window.showInformationMessage('Hello World!');
vscode.window.showInformationMessage('Hello Vsctest!');
```
> 4. Hello World命令重命名
```
// package.json
"contributes": {
  "commands": [
    {
      "command": "extension.helloWorld",
      "title": "MHS: Hello World" //重名
    }
  ]
}
``` 
> 5. 提供一个现实当前时间的命令
```
// src/extension.ts
...
export function activate(context: vscode.ExtensionContext) {
  // nowTime
  let nowTime = vscode.commands.registerCommand('extension.nowTime', () => {
    let myDate = new Date();
    let str = myDate.toLocaleTimeString();
    vscode.window.showErrorMessage(`Time: ${str}`);
  });
  context.subscriptions.push(nowTime);
}

// package.json
"activationEvents": [
  ...,
  "onCommand:extension.nowTime"
],
"contributes": {
  "commands": [
    ...,
    {
      "command": "extension.nowTime",
      "title": "Now Time",
      "category": "MHS"
    }
  ]
},
```
> 调试扩展
> 1. 可设置断点
> 2. vscode bug工具



##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《VSCode 插件开发》]: https://mhsnet.github.io/mhsstudynotes/tools/develop-plug-ins/vscode/index.html "《VSCode 插件开发》"
###
[第一个扩展]: https://mhsnet.github.io/mhsstudynotes/tools/develop-plug-ins/vscode/index.html#get-start-first-extension "第一个扩展"
[扩展分析]: https://mhsnet.github.io/mhsstudynotes/tools/develop-plug-ins/vscode/index.html#get-start-extension-anatomy "扩展分析"