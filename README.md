# MinerProxy
最稳定的ETH/ETC代理中转矿池程序。MinerProxy/矿池代理，支持TCP和SSL协议，支持自定义抽水，高性能高并发，支持web界面管理，包含自启动和进程守护，重启后可以自动运行，会放开防火墙和连接数限制，一键搞定。
# MinerProxy - 使用后算力截图，算力无损耗。
<img width="883" alt="148779614-6ce9006a-6bf3-4c15-87d5-1b3e12ed10b9" src="https://user-images.githubusercontent.com/97756943/149569510-085be8c9-9682-48e7-89be-27975df2bf92.png">

# Liunx-一键安装脚本
好处：适合又想要Linux稳定性的，又不懂Linux的小白的学习者
功能：包含自启动和进程守护，重启后可以自动运行，会放开防火墙和连接数限制，一键搞定
要求：Ubuntu 16+ / Debian 8+ / CentOS 7+ 系统
## V3版本：
使用 root 用户输入下面命令安装或卸载  
```
bash <(curl -s -L https://raw.githubusercontent.com/C4Miner/MinerProxy/main/install.sh)
```
## V4版本
```
bash <(curl -s -L https://raw.githubusercontent.com/C4Miner/MinerProxy/main/v4/install.sh)
```
## 输入命令回车之后一直卡住不动，换这种办法
ubuntu/debian 系统安装
```
wget: apt-get update -y && apt-get install wget -y
```
centos 系统安装
```
yum update -y && yum install wget -y
```
安装好 wget 之后 下载脚本并执行
```
wget https://raw.githubusercontent.com/C4Miner/MinerProxy/main/v4/install.sh
```
```
bash install.sh
```
## 提示 curl: command not found的先安装curl
ubuntu/debian 系统安装 curl 方法:
```
apt-get update -y && apt-get install curl -y
```
centos 系统安装 curl 方法:
```
yum update -y && yum install curl -y
```
安装好 curl 之后就能安装脚本了
# 更新日志
```
2022-05-11   4.0.1>>>优化抽水算法，提高稳定性。
2022-05-10   4.0.0>>>代码重构，提高连接稳定，防CC，优化抽水算法，增加对专业矿机和ETC的支持。
2022-02-15   3.0.3>>>大幅提升稳定性，优化抽水算法，显示矿池延迟，更新UI，抽水百分比现在会按照份额难度换算后呈现，单机2000台压力测试通过。
2021-12-30   1.0.0>>>第一个版本。
```

# 联系邮箱 c4minerproxy@gmail.com


