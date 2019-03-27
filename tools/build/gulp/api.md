# [《MHS 学习笔记》] > [《Gulp 笔记》] > [API] (mhs2019.3.27)

- [series()]
- [parallel()]

## <span id="series">series()</span>
> 顺序执行，可用series(),parallel()嵌套，避免重复任务。
> 语法
```
> series(...tasks) --- 语法
```
> 使用
```
import { series } from 'gulp';
series(taskA, series(), parallel(), ...);
```

## <span id="parallel">parallel()</span>
> 并行执行，可用series(),parallel()嵌套，避免重复任务。
> 语法
```
> parallel(...tasks) --- 语法
```
> 使用
```
import { parallel } from 'gulp';
parallel(taskA, series(), parallel(), ...);
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Gulp 笔记》]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/index.html "《Gulp 笔记》"
[API]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/api.html "API"

[series()]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/api.html#series "series()"
[parallel()]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/api.html#parallel "parallel()"