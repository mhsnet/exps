# 《php》 [Home] (更新 mhs2019.1.22)

###### 1. 安装httpd
```
$ yum install -y httpd24u --- 安装httpd
-i>
配置（/etc/httpd/conf/httpd.conf）
DocumentRoot "/var/www/client-mgr/clt_adm"
<Directory "/var/www/client-mgr">
    AllowOverride None
    Require all granted
</Directory>
<-
```

###### 2. 上传解压文件
```
$ pscp G:\bf\xxx.zip root@xxx.xxx.xxx.xxx:/var --- putty上传文件
$ unzip xxx.zip -d ./ --- 解压文件
```

###### 3. 安装php
```
$ yum install -y mod_php72u
$ yum install -y php72u-mysqlnd
$ yum install -y php72u-json
```
###### 4. 安装mariadb
```
$ yum install -y mariadb101u
$ yum install -y mariadb101u-server
$ mysql_secure_installation
```

