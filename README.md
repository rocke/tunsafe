# 一键脚本搭建TunSafe服务端

1、系统安装为ubuntu >= 16.04

2、建议使用UDP+混淆模式

3、个别地区如果udp限制严重，可选择TCP模式任意一个，但效率比UDP模式低

4、速度比较 UDP > TCP > TCP + HTTPS

首先连接VPS，使用以下一键脚本安装

> wget https://raw.githubusercontent.com/atrandys/tunsafe/master/tunsafe_install.sh && chmod +x tunsafe_install.sh && >./tunsafe_install.sh

在弹出的页面中选择1 安装tunsafe
[img]https://www.atrandys.com/wp-content/uploads/2019/02/tunsafe1.png[/img]


安装过程中需要你选择使用哪种模式，建议1 UDP模式，如果UDP干扰严重，可选择TCP中的一个，https比tcp还要慢一点



安装完成后在/etc/tunsafe/目录下可看到client.conf，这个就是客户端配置文件。

客户端安装TunSafe
windows版：

下载安装TunSafe，这是一个windows端的第三方客户端，因为官方windows版本的还没开发完成，先用这个软件代替，TunSafe已经开源了，可以放心使用。

注意下载TunSafe 1.5-rc2版本，其他版本不支持混淆。

官网下载：TunSafe

打开TunSafe，点击file，选择import file，选择第5步下载的client.conf文件，导入到软件中。



导入后会自动连接，连接成功后，所有流量都会被代理，也就是全局代理。

移动版
移动客户端暂不支持混淆的TunSafe，等待客户端更新。

多用户
./tunsafe_install.sh
使用以上命令，输入需要增加的用户名，不可输入client，不要和已经存在的用户重复即可。
