# [《MHS 学习笔记》] > [《Gulp 笔记》] > [讲解Globs] (mhs2019.3.27)

- [Glob描述]
- [使用]

## <span id="description">Glob描述</span>
> 1. glob --- 匹配文件路径的字符串|通配符
> 2. src() --- glob或[glob, ...]确定pipe操作哪些文件

## <span id="use">使用</span>
> 1. 避免使用Node路径方法
```
/ --- 分隔符
\\ --- 转义
* --- 0-n字符
** --- 0-n分段
! --- 否认
'src/hello\\*.js' --- 转义*
['script/**/*.js', '!scripts/vendor/', 'scripts/vendor/react.js'] --- 最后的不去除
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Gulp 笔记》]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/index.html "《Gulp 笔记》"
[讲解Globs]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/explain-globs.html "讲解Globs"

[Glob描述]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/explain-globs.html#description "Glob描述"
[使用]: https://mhsnet.github.io/mhsstudynotes/tools/build/gulp/explain-globs.html#use "使用"