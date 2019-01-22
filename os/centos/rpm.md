# 《rpm》 [Home] (更新 mhs2019.1.21)

```
$ rpm -ivh <pkgn> --- 安装1个包
$ rpm -qa [*xxx*] --- 已安装的软件
$ rpm -qf <path> --- 文件属于哪个包[绝对路径]
$ rpm -ql <pkgn> --- 安装在何处
$ rpm -qi <pkgn> --- 信息
$ rpm -qc <pkgn> --- 配置文件
$ rpm -qd <pkgn> --- 文档
$ rpm -qR <pkgn> --- 依赖
$ rpm -Uvh <pkgn> --- 升级1个包
$ rpm --import IUS-COMMUNITY-GPG-KEY --- 导入秘钥
$ wget --no-check-certificate <xxx.rpm> --- 跳过验证获取包
```