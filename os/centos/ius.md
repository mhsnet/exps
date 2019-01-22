# 《ius》 [Home] (更新 mhs2019.1.21)

###### 1. 安装EPEL仓库
```
$ yum info epel-release --- 查看epel
$ yum -y install epel-release --- 安装epel库
$ yum clean all --- 清楚yum缓存
$ yum makecache --- 建立缓存
```

###### 2. 安装IUS仓库
```
$ wget --no-check-certificate https://centos7.iuscommunity.org/ius-release.rpm --- 下载ius包
$ wget --no-check-certificate https://dl.iuscommunity.org/pub/ius/IUS-COMMUNITY-GPG-KEY --- 下载秘钥
$ rpm -ivh ius-release.rpm --- 安装ius
$ rpm --import IUS-COMMUNITY-GPG-KEY --- 导入秘钥
$ cd /etc/yum.repos.d --- 查看源目录
$ vi ius.repo --- 设置国内源（baseurl=https://mirrors.tuna.tsinghua.edu.cn/ius/stable/CentOS/7/$basearch）
$ yum clean all --- 清楚yum缓存
$ yum makecache --- 建立缓存
```

###### 3. 资源
<https://ius.io/>
<https://mirrors.tuna.tsinghua.edu.cn/ius/>