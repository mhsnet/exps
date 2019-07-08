# [《MHS 学习笔记》] > [《Win10》] > scoop (mhs2019.7.8)

- 安装
```
> win + r(快捷键) -> powershell(输入)
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
> scoop help
```
- 常用命令
```
> scoop help --- 查看命令帮助
> scoop update [appN|*] --- 更新自身[更新应用|全部安装应用]
> scoop search [appN|cmdN] --- 查找[应用|指令]
> scoop install appN --- 安装应用
> scoop list --- 查看已安装软件
```

#
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Win10》]: https://mhsnet.github.io/mhsstudynotes/os/win10/index.html "《Win10》"