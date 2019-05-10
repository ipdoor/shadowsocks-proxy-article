@[TOC](安装ss,尽量折腾！对自己好一点儿。 •̀ ω •́ )
## Install
# Ubuntu 16.04 安装shadowsocks-libev
>For Ubuntu 14.04 and 16.04 users, please install from PPA:
```
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:max-c-lv/shadowsocks-libev -y
sudo apt-get update
sudo apt install shadowsocks-libev
```
## Usage
# 查看/etc/shadowsocks-libev/config.json
```
vim /etc/shadowsocks-libev/config.json
```
>>脚本默认显示结果为：
>{
    "server":"127.0.0.1“，// <font color=red >修改本地回环地址，填写自己的代理服务器的IP地址</font>
    "server_port":8388,
    "local_port":1080,
    "password":"attubeor",
    "timeout":60,
    "method":"chacha20-ietf-poly1305"
}


# 运行config.json并且查看运行status
```
sudo systemctl start shadowsocks-libev-server@config //运行config脚本有关信息。
```
```
sudo systemctl status shadowsocks-libev-server@config //查看ss proxy运行的状态是否正常。
```
* <font color=red>注意</font>
    >避免使用ss预留的默认端口号```8388```，改成自定义端口号。//使用默认端口号，代理容易被ban。  
* <font color=red>如何查询端口服务正常运行</font>
    **检测<u>国内</u>流量运行状态，访问：[站长工具-端口扫描](http://tool.chinaz.com/port/)**
    **检测<u>国外</u>流量运行状态，访问：[Check a port's status](https://www.yougetsignal.com/tools/open-ports/)**
>人生苦短，少走弯路，总结经验，才是王道。
