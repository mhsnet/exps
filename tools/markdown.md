# **<span id="markdown">《Markdown 语法》</span>** [工具] tools-markdown-v1.0.0(mhs2018.10.11)

- [概述]
  - [宗旨]
  - [兼容HTML]
  - [特殊字符自动转换]
- [块元素]
  - [段落和换行]
  - [标题]
  - [块引用]
  - [列表]
  - [代码块]
  - [水平线]
- [段元素]
  - [链接]
  - [强调]
  - [代码]
  - [图片]
- [其它]
  - [自动链接]
  - [反斜杠]
  - [资源]

------

# **<span id="overview">《概述》</span> [Markdown 语法] [宗旨] [兼容HTML] [特殊字符自动转换]**

## **<span id="philosophy">宗旨</span> [Markdown 语法] [概述]**
> 易读易写

## **<span id="inline-html">兼容HTML</span> [Markdown 语法] [概述]**
> - 前后空行
> - 开始结尾不缩进
```

<table>
  <tr><td>h1</td></tr>
</table>

```

## **<span id="automatic-escaping">特殊字符自动转换</span> [Markdown 语法] [概述]** 
> < & &copy;
```
< & &copy;
```

------

# **<span id="block-elements">《块元素》</span> [Markdown 语法] [段落和换行] [标题] [块引用] [列表] [代码块] [水平线]**

## **<span id="paragraphs-line">段落和换行</span> [Markdown 语法] [块元素]**
> - 段落 - 前后有空行
> - 换行 - 使用[块引用]和列表

## **<span id="headers">标题</span> [Markdown 语法] [块元素]**
```
# h1 ## h2 ### h3 #### h4 ##### h5 ###### h6
```

## **<span id="block-quotes">块引用</span> [Markdown 语法] [块元素]**
> 块1
> > 块1-1

块外
```
> 块1
> > 块1-1

块外
```

## **<span id="lists">列表</span> [Markdown 语法] [块元素]**
> - 1
>   1. 1-1
> - 2
>   - 2-1
```
- 1
  1. 1-1
- 2
  - 2-1
```

## **<span id="code-blocks">代码块</span> [Markdown 语法] [块元素]**
> \`\`\`
> 
> code
> 
> \`\`\`
```
code
``` 

## **<span id="horizontal-rules">水平线</span> [Markdown 语法] [块元素]**
> ---
```  
---
```

------

# **<span id="span-elements">《段元素》</span> [Markdown 语法] [链接] [强调] [代码] [图片]**

## **<span id="links">链接</span> [Markdown 语法] [段元素]**
> [Markdown 语法]
> [块元素]
```  
[Markdown 语法]
[Markdown 语法]: https://mhsnet.github.io/note/tools/markdown.html "Markdown 语法"
[块元素]
<span id="block-elements">《块元素》</span>
[块元素]: https://mhsnet.github.io/note/tools/markdown.html#block-elements "块元素(Block Elements)"
```

## **<span id="emphasis">强调</span> [Markdown 语法] [段元素]**
> **强调**
```  
**强调**
```

## **<span id="code">代码</span> [Markdown 语法] [段元素]**
> `代码`
```
`代码`
```

## **<span id="images">图片</span> [Markdown 语法] [段元素]**
> ![图片替换文字][图片1]
```
![图片替换文字][图片1]
[图片1]: http://localhost:9098/images/img1.png "图片1(img1.png)"
```

---

# **<span id="miscellaneous">《其它》</span> [Markdown 语法] [自动链接] [反斜杠] [资源]**

## **<span id="automatic-links">自动链接</span> [Markdown 语法] [其它]**
> <http://localhost:9098/tools/markdown>
```
<http://localhost:9098/tools/markdown>
```

## **<span id="backslash-escapes">反斜杠</span> [Markdown 语法] [其它]**
> \`
> \*
> \_
> \{
> \}
> \[
> \]
> \(
> \)
> \#
> \+
> \-
> \.
> \!
```
\`
```

## **<span id="resources">资源</span> [Markdown 语法] [其它]**
> - <https://daringfireball.net/projects/markdown/>
> - Markdown PDF - vscode插件
> - Markdown All in One - vscode插件 

#
[我的技术栈学习笔记]: https://mhsnet.github.io/note/ "我的技术栈学习笔记"
[Markdown 语法]: https://mhsnet.github.io/note/tools/markdown.html "Markdown 语法"

[概述]: https://mhsnet.github.io/note/markdown.html#overview "概述(Overview)"
[宗旨]: https://mhsnet.github.io/note/tools/markdown.html#philosophy "宗旨(Philosophy)"
[兼容HTML]: https://mhsnet.github.io/note/tools/markdown.html#inline-html "兼容HTML(Inline HTML)"
[特殊字符自动转换]: https://mhsnet.github.io/note/tools/markdown.html#automatic-escaping "特殊字符自动转换(Automatic Escaping for Special Characters)"

[块元素]: https://mhsnet.github.io/note/tools/markdown.html#block-elements "块元素(Block Elements)"
[段落和换行]: https://mhsnet.github.io/note/tools/markdown.html#paragraphs-line "段落和换行(Paragraphs And Line Breaks)"
[标题]: https://mhsnet.github.io/note/tools/markdown.html#headers "标题(Headers)"
[块引用]: https://mhsnet.github.io/note/tools/markdown.html#block-quotes "块引用(Block Quotes)"
[列表]: https://mhsnet.github.io/note/tools/markdown.html#lists "列表(Lists)"
[代码块]: https://mhsnet.github.io/note/tools/markdown.html#code-blocks "代码块(Code Blocks)"
[水平线]: https://mhsnet.github.io/note/tools/markdown.html#horizontal-rules "水平线(Horizontal Rules)"

[段元素]: https://mhsnet.github.io/note/tools/markdown.html#span-elements "段元素(Span Elements)"
[链接]: https://mhsnet.github.io/note/tools/markdown.html#links "链接(Links)"
[强调]: https://mhsnet.github.io/note/tools/markdown.html#emphasis "强调(Emphasis)"
[代码]: https://mhsnet.github.io/note/tools/markdown.html#code "代码(Code)"
[图片]: https://mhsnet.github.io/note/tools/markdown.html#images "图片(Images)"

[其它]: https://mhsnet.github.io/note/tools/markdown.html#miscellaneous "其它(Miscellaneous)"
[自动链接]: https://mhsnet.github.io/note/tools/markdown.html#automatic-links "自动链接(Automatic Links)"
[反斜杠]: https://mhsnet.github.io/note/tools/markdown.html#backslash-escapes "反斜杠(Backslash Escapes)"
[资源]: https://mhsnet.github.io/note/tools/markdown.html#resources "资源(Resources)"

[图片1]: http://localhost:9098/images/img1.png "图片1(img1.png)"