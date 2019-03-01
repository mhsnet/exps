# YUM [《MHS 学习笔记》] -> [《CentOS7》]  (mhs2019.3.1)

- [YUM源]

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

[YUM源]: https://mhsnet.github.io/note/os/centos7/others/yum.html#yum-repository "YUM源"