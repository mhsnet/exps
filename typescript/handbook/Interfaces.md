# [《MHS 学习笔记》] > [《TypeScript 手册》] > [接口] (mhs2019.3.28)

- [介绍]
- [探索]
- [可选属性]
- [只读属性]
- [额外属性检查]
- [函数类型]
- [可索引类型]
- [类类型]

## <span id="introduction">介绍</span>
> 1. TypeScript核心原则之一，对值进行类型检查（duck typing）。
> 2. 接口为这些类型命名，为代码|外部代码提供约定。

## <span id="exploration">探索</span>
> 1. 传入参数使用接口定义
> 2. 传入多个属性，不按顺序只检查必须属性及其类型，有时并不会如此宽松
```
// examples/typescript/handbook/
$ gulp taskInterfacesA
// 接口People
// : --- 属性
// ?: --- 可选属性
// readonly --- 只读
// ReadonlyArray --- 数组不可变
// propName --- 添加字符串索引签名
interface People {
  name: string;
  readonly type?: string;
  labels?: ReadonlyArray<string>;
  age?: number;
  [propName: string]: any;
}
// 函数
function printName(user: interfaces.People) {
  if (user.age) { 
    console.log(user.age);
  }
  console.log(user.name);
}
// 测试使用
let userN = { name: 'Name1' };
testF.interfaces.printName(userN);
```
## <span id="optional-properties">可选属性</span>
> 1. 接口属性可选
> 2. 描述可用属性，捕获引用不存在属性时错误
```
// examples/typescript/handbook/
$ gulp taskInterfacesA
```
## <span id="readonly-properties">只读属性</span>
> 1. 对象属性只在创建时修改
> 2. 可赋值对象字面量
> 3. ReadonlyArray<T> --- 确保数组创建后不被修改,也不能用于赋值给数组
> 4. ReadonlyArray<T> --- 可用类型断言as修改，用于赋值给数组
> 5. readonly|const --- 用于属性|变量
```
// examples/typescript/handbook/
$ gulp taskInterfacesB
let labels: string[] = [];
let user: testI.People = { type: 'user', labels: ['cs'], name: 'Name1' };
// error
// user.type = 'user';
// user.labels[1] = 'cs2';
// labels = user.labels;
//testF.interfaces.printName({ type: 'user', name: 'Name1', ages: 12 });
labels = user.labels as string[];
console.log(labels);
cb();
```
## <span id="excess-property-checks">额外属性检查</span>
> 1. 对象字面量会被特殊对待，存在接口不包含属性报错。
> 2. 解决：as|propName|赋值给另一个变量
```
$ gulp taskInterfacesB
```
## <span id="function-types">函数类型</span>
> 1. 创建1个函数类型变量，将同类型函数赋值给这个变量。
> 2. 参数不需与接口名字相同，会逐个类型检查
> 3. 返回值推断检查
```
// 接口
interface TestFunc {
  (name: string, age: number): boolean;
}
function taskInterfacesC(cb) {
  // 函数类型
  let testFunc: testI.InterfaceTestFunc;
  testFunc = function (name, age) {
    console.log(name);
    return true;
  }
  testFunc('n1', 11);
  cb();
};
```

## <span id="indexable-types">可索引类型</span>
> 1. 2种索引签名：字符串和数字。
> 2. 常用于Array和Describe，可设readonly。
```
// 可索引类型接口1
interface TestArr {
  [index: number]: string;
}
// 可索引类型接口2
interface TestDict {
  readonly [index: string]: string;
}
function taskInterfacesD(cb) {
  // 索引类型
  let TestArr: testI.Interfaces.TestArr;
  TestArr = ['a1', 'a2'];
  console.log(TestArr[0]);
  let TestDict: testI.Interfaces.TestDict;
  TestDict = { 'n1': 'v1', 'n2': 'v2' };
  // error --- readonly
  // TestDict.n2 = 'v3';
  console.log(TestDict.n2);
  cb();
};
```

## <span id="class-types">类类型</span>

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《TypeScript 手册》]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/index.html "《TypeScript 手册》"
[接口]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html "接口"

[介绍]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html#introduction "介绍"
[探索]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html#exploration "探索"
[可选属性]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html#optional-properties "可选属性"
[只读属性]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html#readonly-properties "只读属性"
[额外属性检查]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html#excess-property-checks "额外属性检查"
[函数类型]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html#function-types "函数类型"
[可索引类型]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html#indexable-types "可索引类型"
[类类型]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/interfaces.html#class-types "类类型"