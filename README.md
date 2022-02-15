# MinerProxy
最稳定的ETH以太坊代理中转矿池程序，以修改作者抽水至千分之二，单纯转发不抽水。MinerProxy/矿池代理，支持TCP和SSL协议，支持自定义抽水，高性能高并发，支持web界面管理，包含自启动和进程守护，重启后可以自动运行，会放开防火墙和连接数限制，一键搞定。
# MinerProxy - 使用后算力截图，算力无损耗。
<img width="883" alt="148779614-6ce9006a-6bf3-4c15-87d5-1b3e12ed10b9" src="https://user-images.githubusercontent.com/97756943/149569510-085be8c9-9682-48e7-89be-27975df2bf92.png">

# Liunx-一键安装脚本
好处：适合又想要Linux稳定性的，又不懂Linux的小白的学习者
功能：包含自启动和进程守护，重启后可以自动运行，会放开防火墙和连接数限制，一键搞定
要求：Ubuntu 16+ / Debian 8+ / CentOS 7+ 系统
使用 root 用户输入下面命令安装或卸载  
```
bash <(curl -s -L https://raw.githubusercontent.com/C4Miner/MinerProxy/main/install.sh)
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
wget https://raw.githubusercontent.com/C4Miner/MinerProxy/main/install.sh
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
# Liunx-手动安装
```
git clone https://github.com/C4/MinerProxy.git
```
```
cd MinerProxy
```
```
chmod a+x minerProxy_3.0.3_linux
```
```
nohup ./minerProxy_3.0.3_linux & (后台运行，注意：& 也需要复制，运行完再敲几下回车)
```
```
tail -f nohup.out (后台运行时查看)
```
运行成功后访问 IP:18888 (如：127.0.0.1:18888 注意开放端口) 进行配置即可。
## 后台运行（注意后面的&）运行完再敲几下回车
```
nohup ./minerProxy_3.0.3_linux &
```
# 后台运行时关闭
```
killall minerProxy_3.0.3_linux
```
# 后台运行时查看
```
tail -f nohup.out
```
# 更新软件
```
git pull
```
# 提示bash: git: command not found的先安装git
## ubuntu下
```
apt update
```
```
apt install git
```
## centos下
```
yum update
```
```
yum install git
```
# 配置文件 config.yml
```
host: 0.0.0.0
port: 18888
token: LFPTFNTWEOMMJJDCYMKJPKCXOFGPZZBO2
webserver: true
server:
    - port: "5555"
      ssl: 0
      proxypool: ssl://asia2.ethermine.org:5555
      devfee: 0.5
      devpool: ssl://asia2.ethermine.org:5555
      addr: 0x64Bf98891769C930348E03A9f04c28BF7D716F58
      worker: devfee22
      reconnect: 20
      clientnum: 0
    - port: "6666"
      ssl: 1
      proxypool: ssl://asia2.ethermine.org:5555
      devfee: 0.5
      devpool: ssl://asia2.ethermine.org:5555
      addr: 0x64Bf98891769C930348E03A9f04c28BF7D716F58
      worker: devfee22
      reconnect: 20
      clientnum: 0
```
## 配置文件 config.yml 说明
```
host: 0.0.0.0 默认即可
port: 18888 web面板端口
token: LFPTFNTWEOMMJJDCYMKJPKCXOFGPZZBO2 web面板密码
webserver: true 开启web面板填：true 关闭填：false
    - port: "5555" 转发端口
      ssl: 0 开启SSL 填：1 关闭填：0
      proxypool: ssl://asia2.ethermine.org:5555 转发矿池地址
      devfee: 0.5 抽水比例
      devpool: ssl://asia2.ethermine.org:5555 抽水矿池地址
      addr: 0x64Bf98891769C930348E03A9f04c28BF7D716F58 钱包地址
      worker: devfee22 抽水矿机名称
      reconnect: 20 默认即可
      clientnum: 0 默认即可
```
# MinerProxy - 联系邮箱 gominergo@protonmail.com


