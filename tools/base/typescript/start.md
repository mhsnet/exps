# [《MHS 学习笔记》] > [《TypeScript 笔记》] > 开始 (mhs2019.3.26)

- [安装TypeScript]
- [ts文件]
- [Web运行]

## <span id="install">安装TypeScript</span>
```
$ yarn global list --depth=0
$ yarn global add typescript
```
## <span id="ts-file">ts文件</span>
> www_test/ts/hello.ts
```
// 类
// public --- 创建同名成员变量
class Student {
  name: string;

  constructor(name: string, public age: number) {
    this.name = name;
  }
}

// 接口
interface Person {
  name: string;
}

// 注解
function hello(person: Person) {
  return `Hello ${person.name}!`;
}

let user = new Student('stdN1', 13);

document.body.innerHTML = hello(user);
```
> 编译代码
```
$ tsc hello.ts
```
## <span id="web-run">Web运行</span>
> www_test/ts/hello.html
```
<!DOCTYPE html>
<html>

<head>
  <title>TypeScript Hello</title>
</head>

<body>
  <script src="hello.js"></script>
</body>

</html>
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《TypeScript 笔记》]: https://mhsnet.github.io/mhsstudynotes/tools/base/typescript/index.html "《TypeScript 笔记》"
[开始]: https://mhsnet.github.io/mhsstudynotes/tools/base/typescript/start.html "开始"

[安装TypeScript]: https://mhsnet.github.io/mhsstudynotes/tools/base/typescript/start.html#install "安装TypeScript"
[ts文件]: https://mhsnet.github.io/mhsstudynotes/tools/base/typescript/start.html#ts-file "ts文件"
[Web运行]: https://mhsnet.github.io/mhsstudynotes/tools/base/typescript/start.html#web-run "Web运行"