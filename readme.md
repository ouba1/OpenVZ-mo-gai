

```bash
# this is for Debian 8
wget https://raw.githubusercontent.com/ouba1/OpenVZ-mo-gai/master/tcp_nanqinlang-haproxy-debian.sh
bash tcp_nanqinlang-haproxy-debian.sh
```

```bash
# this is for CentOS 6/7
wget https://raw.githubusercontent.com/ouba1/OpenVZ-mo-gai/master/tcp_nanqinlang-haproxy-centos.sh
bash tcp_nanqinlang-haproxy-centos.sh
```
以下进行脚本使用说明：

安装 lkl-haproxy

此命令用于安装 lkl-haproxy。

在 /home/tcp_nanqinlang 进行安装，所以安装完成后不要动这个文件夹了（除非你想修改端口）。

安装过程中，会提示你选择单个端口或端口段输入，具体已在运行脚本的提示中有说明，这里不再赘述。

安装完成后，会开启 lkl-haproxy。以后重启机器也会随开机自启。

以后若需要修改转发端口，请将 /home/tcp_nanqinlang/haproxy.cfg 中的端口号和 /home/tcp_nanqinlang/redirect.sh 中的端口号改为你想要的端口或端口段，修改完成后重启服务器。

使用前请注意自己的 iptables 相关设置。

检查 lkl-haproxy 运行状态

此命令用于检查 lkl-haproxy 运行与否，可通过返回的提示判断。

卸载 lkl-haproxy

运行此命令会卸载 haproxy、删除 /home/tcp_nanqinlang、移除 rc.local 开机自启项。稍后请自行移除 iptables 相关规则。
## according

update details  
https://github.com/nanqinlang/tcp_nanqinlang/releases

中文文档  
https://sometimesnaive.org/shell-tcp_nanqinlang.html
