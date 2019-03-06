# 《Git 使用》 [Home] (更新 mhs2019.1.15)

- [使用]
  1. [github使用]
    - 1-1. 创建资源
  2. [vscode使用]
    - 1-1. 克隆资源
    - 1-2. 上传本地项目
  3. [分支管理]
  

## <span id="use">使用</span> [Top]

### 1. <span id="github">github</span> [Top]
###### 1-1. 创建资源
```
1. + -> New repository
2. Repository name (ep: note)
3. Description (ep: note)
4. Create repository
```

### 2. <span id="vscode">vscode</span> [Top]
###### 1-1. 克隆资源
```
Ctrl+Shift+P -> Git:Clone
$ git config -l
$ git config user.name "mhsnet"
$ git config user.email "mhsnet@163.com"
```
###### 1-2. 上传本地项目
```
$ git init
$ git config user.name "mhsnet"
$ git config user.email "mhsnet@163.com"
$ git remote add origin https://github.com/mhsnet/*.git
```

### 3. <span id="branch">分支管理</span> [Top]
```
# git branch --- 查看分支
# git branch -r --- 查看远程分支
# git branch -a --- 查看所有分支
# git branch <name> --- 创建分支
# git fetch --- 更新信息
# git push origin <name> --- 创建远程分支
# git checkout <name> --- 切换分支
# git checkout -t <origin/name> --- 切换远程分支
# git merge --no-ff -m "merge with dev" dev --- 合并分支
# git branch -D <name> --- 删除本地分支
# git push origin -d <name> --- 删除远程分支
# git remote -v --- 抓取和推送的origin的地址
# git log --graph --pretty=oneline --abbrev-commit --- 查看日（分支）
```

##
[Home]: https://mhsnet.github.io/mhsstudynotes/ "《MHS技术栈学习笔记》"

[Top]: https://mhsnet.github.io/mhsstudynotes/tools/git.html "《Git 使用》"

[使用]: https://mhsnet.github.io/mhsstudynotes/tools/git.html#use "《Git 使用》"
[github使用]: https://mhsnet.github.io/mhsstudynotes/tools/git.html#github "github使用"
[vscode使用]: https://mhsnet.github.io/mhsstudynotes/tools/git.html#vscode "vscode使用"
[分支管理]: https://mhsnet.github.io/mhsstudynotes/tools/git.html#branch "分支管理"


