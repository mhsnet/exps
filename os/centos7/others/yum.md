# YUM [《MHS 学习笔记》] -> [《CentOS7》]  (mhs2019.3.1)

- [YUM指令]
- [RPM]
- [YUM源]

## <span id="yum-cmd">YUM指令</span> [YUM]
> ```
> $ yum list [available|installed|extras|updates|obsoletes|all|recent] [pkgspec] xxx*xxx | less
> $ yum search <schstr> --- 收索包名和描述含收索字符
> $ yum info <pkgn> --- 显示包详情
> $ yum install [-y] <pkgn> --- 安装包[不询问]
> $ yum update [-y] <pkgn> --- 升级包[不询问]
> $ yum remove [-y] <pkgn> --- 删除包[不询问] 搜索已安装包
> $ yum group list --- 查看可用group
> $ yum groupinstall <"Development Tools"> --- 安装group包
> $ yum groupupdate <"Development Tools"> --- 升级group包
> $ yum groupremove <"Development Tools"> --- 删除group包
> $ yum repolist --- 查看系统使用仓库
> $ yum provides /etc/httpd/conf/httpd.conf --- 查看文件属于哪个软件包
> $ yum clean all --- 删除缓存
> $ yum history --- 查看最近执行的命令
> $ yum history undo 6 --- 撤销某个动作
> ```

## <span id="rpm">RPM</span> [YUM]
> ```
> $ rpm -qa --- 已安装的软件
> $ rpm -qf <path> --- 文件属于哪个包[绝对路径]
> $ rpm -ql <pkgn> --- 安装在何处
> $ rpm -qi <pkgn> --- 信息
> $ rpm -qc <pkgn> --- 配置文件
> $ rpm -qd <pkgn> --- 文档
> $ rpm -qR <pkgn> --- 依赖
> ```

## <span id="yum-repository">YUM源</span> [YUM]
> 删除YUM源(如nodejs源)：
> ```
> $ cd /etc/yum.repos.d/ --- 源目录
> $ ls
> $ rm nodesource-el7.repo
> $ ls /etc/pki/rpm-gpg/ --- 删除库
> $ rm /etc/pki/rpm-gpg/NODESOURCE-GPG-SIGNING-KEY-EL --- 删除库
> $ rpm -qa | grep node
> $ yum remove nodesource-release-el7-1.noarch --- 删除rpm包
> $ yum remove libvirt-daemon-driver-nodedev-3.9.0-14.el7_5.4.x86_64 --- 删除rpm包
> $ yum repolist --- 查看源
> $ yum-config-manager --enable nodesource
> $ yum-config-manager --disable nodesource
> $ yum clean all --- 清理yum缓存
> $ yum makecache --- 更新源
> ```

> 添加nodejs源（https://github.com/nodesource/distributions）
> ```
> $ curl -sL https://rpm.nodesource.com/setup_10.x | bash -
> $ yum clean all
> $ yum makecache
> $ yum info nodejs
> ```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/note/ "《MHS 学习笔记》"
[《CentOS7》]: https://mhsnet.github.io/note/os/centos7/index.html "《CentOS7》"
[YUM]: https://mhsnet.github.io/note/os/centos7/others/yum.html "YUM"

[YUM指令]: https://mhsnet.github.io/note/os/centos7/others/yum.html#yum-cmd "YUM指令"
[RPM]: https://mhsnet.github.io/note/os/centos7/others/yum.html#rpm "RPM"
[YUM源]: https://mhsnet.github.io/note/os/centos7/others/yum.html#yum-repository "YUM源"