# 《Markdown 语法》 [Home] (mhs2019.1.15)

- [兼容HTML]
- [块元素]
  1. [段落和换行]
  2. [标题]
  3. [块引用]
  4. [列表]
  5. [代码块]
  6. [水平线]
- [段元素]
  1. [链接]
  2. [强调]
  3. [代码]
  4. [图片]
- [资源]

## <span id="inline-html">兼容HTML</span>[Top]
> - 前后空行
> - 开始结尾不缩进
> - 特殊字符可以在HTML|Code中显示

<table>
  <tr><th>h1</th><th>h2</th></tr>
  <tr><td>d1-1</td><td>2 > 1</td></tr>
  <tr><td>d2-1</td><td>&</td></tr>
</table>

```

<table>
  <tr><th>h1</th><th>h2</th></tr>
  <tr><td>d1-1</td><td>2 > 1</td></tr>
  <tr><td>d2-1</td><td>&</td></tr>
</table>

```

## <span id="block-elements">块元素</span> [Top]

### 1. <span id="paragraphs-line">段落和换行</span> [Top]
> - 段落 - 前后有空行
> - 换行 - 使用[块引用]和[列表]

### 2. <span id="headers">标题</span> [Top]
```
# h1 ## h2 ### h3 #### h4 ##### h5 ###### h6
```

### 3. <span id="block-quotes">块引用</span> [Top]
> 块1
> > 块1-1

块外
```
> 块1
> > 块1-1

块外
```

### 4. <span id="lists">列表</span> [Top]
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

### 5. <span id="code-blocks">代码块</span> [Top]
> \`\`\`
> 
> code
> 
> \`\`\`
```
code
``` 

### 6. <span id="horizontal-rules">水平线</span> [Top]
> ---
```  
---
```

## <span id="span-elements">段元素</span> [Top]

### 1. <span id="links">链接</span> [Top]
> [Top]
> [块元素]
> <https://mhsnet.github.io/note/>
```  
[Top]: https://mhsnet.github.io/note/tools/markdown.html "Markdown 语法"
<span id="block-elements">xxx</span>
[块元素]: https://mhsnet.github.io/note/tools/markdown.html#block-elements "块元素(Block Elements)"
<https://mhsnet.github.io/note/>
```

### 2. <span id="emphasis">强调</span> [Top]
> **强调**
```  
**强调**
```

### 3. <span id="code">代码</span> [Top]
> 代码`><=&`
```
`><=&`
```

### 4. <span id="images">图片</span> [Top]
> ![图片替换文字][图片mdcs]
```
![图片替换文字][图片mdcs]
[图片mdcs]: https://mhsnet.github.io/note/imgs/mdcs.png "图片(mdcs.png)"
```

## <span id="resources">资源</span> [Top]
> - <https://daringfireball.net/projects/markdown/>
> - Markdown PDF - vscode插件
> - Markdown All in One - vscode插件 

##
[Home]: https://mhsnet.github.io/note/ "《MHS技术栈学习笔记》"

[Top]: https://mhsnet.github.io/note/tools/markdown.html "《Markdown 语法》"

[兼容HTML]: https://mhsnet.github.io/note/tools/markdown.html#inline-html "兼容HTML(Inline HTML)"

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

[资源]: https://mhsnet.github.io/note/tools/markdown.html#resources "资源(Resources)"

[图片mdcs]: https://mhsnet.github.io/note/imgs/mdcs.png "图片(mdcs.png)"