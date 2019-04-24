# [《MHS 学习笔记》] > [《TypeScript 学习》] > [模块] (mhs2019.4.23)

- [介绍]
- [导出]
- [导入]

## <span id="introduction">介绍</span>
> 1. 模块（外部模块）和命名空间（内部模块）
> 2. 模块自声明，在自身作用域执行，含顶级import|export的文件当成模块，相反全局可见（对模块也可见）
> 3. 2个模块关系在文件级使用export和import建立
> 4. 尽可能顶层导出
> 5. 导出单个,使用 export default
> 6. 导出多个放顶层，导入明确名字
> 7. 导出大量，导入使用命名空间模式
> 8. 使用重新导出进行扩展

## <span id="export">导出</span>
> 1. 可导出任何声明(variable|function|class|type alias|interface)
```
export interface Xx {};
export class Xx {}
export const xXx = ...;
export function xXx(){}
```
> 2. 导出语句(方便重命名)
```
export { Xx, xX };
export { Xx as Xx };
```
> 3. 重新导出
```
export {Xx as Xx} from "./xxx";
```
> 4. 包裹多个模块并把它们导出内容放一起
```
export * from "./xxx";
export * from "./xxx";
```
> 5. 默认导出(支持ES6)
```
export default xxx;
```
> 6. 默认导出(支持CommonJS|AMD)
```
export = xxx;
```

## <span id="import">导入</span>
> 1. 导入模块中某个内容，可重命名
```
import { Xx as Xx } from "./xxx";
```
> 2. 整个模块导入变量
```
import * as xxx from "./xxx";
```
> 3. 有副作用的导入(全局状态)
```
import "./xxx.js";
```
> 4. 导入默认(支持ES6)
```
import xxx from "./xxx";
```
> 5. 导入默认(支持CommonJS|AMD)
```
import xxx = require("./xxx");
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《TypeScript 学习》]: https://mhsnet.github.io/mhsstudynotes/typescript/index.html "《TypeScript 学习》"
##
[模块]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/modules.html "模块"
###
[介绍]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/modules.html#introduction "介绍"
[导出]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/modules.html#export "导出"
[导入]: https://mhsnet.github.io/mhsstudynotes/typescript/handbook/modules.html#import "导入"