# 《yum》 [Home] (更新 mhs2019.1.21)

```
$ yum clean all --- 清除yum缓存
$ yum info <pkgn> --- 显示包详情
$ yum install [-y] <pkgn> --- 安装包
$ yum list [available|installed|...] [x*x] --- 列出软件包
$ yum makecache --- 建立yum缓存
$ yum remove [-y] <pkgn> --- 删除安装的库
$ yum repolist all --- 查看库
$ yum update [-y] <pkgn> --- 升级包[不询问]
$ yum-config-manager --disable <repn> --- 禁用库
$ yum-config-manager --enable <repn> --- 启用库
```