yah3c
=====

本项目修改自 [YaH3C](http://github.com/humiaozuzu/YaH3C).
修改是为了便于打包成 [Arch Linux](https://www.archlinux.org/) 的 [AUR](https://aur.archlinux.org/packages/yah3c/).

安装
------------

推荐使用 `yaourt` 安装:

``` bash
yaourt -S yah3c
```

其他安装工具见 [AUR helpers - ArchWiki](https://wiki.archlinux.org/index.php/AUR_helpers).
你也可以 [手动安装](https://wiki.archlinux.org/index.php/Arch_User_Repository#Installing_packages).

配置
---------

用户的登陆信息按照如下的格式保存在文件`/etc/yah3c.conf`中：

``` ini
[account]                  # 你的帐户
password = 123456          # 密码
ethernet_interface = eth0  # 使用的网卡，默认为eth0
dhcp_command = dhcpcd      # 验证成功后使用的dhcp命令(dhcpcd/dhclient)，默认为空
daemon = True              # 验证成功后是否变成daemon进程，默认为是
```

使用
-----------

``` bash
sudo yah3c -u account
```

Thanks
------

* [humiaozuzu](https://github.com/humiaozuzu) - Original repo [YaH3C](https://github.com/humiaozuzu/YaH3C)
* [qiao](https://github.com/qiao) - Write python installation script for YaH3C
* [houqp](https://github.com/houqp) - Refered to houqp's [pyh3c](https://github.com/houqp/pyh3c)
* [tigersoldier](https://github.com/tigersoldier) - Write EAP-Md5 for YaH3C

License
-------

YaH3C的代码使用MIT License发布，此外，禁止使用YaH3C以及YaH3C的修改程序用于商业目的（比如交叉编译到路由进行销售等行为）
