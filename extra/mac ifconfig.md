## lo

```
# loopback 本机主机地址
# flag=8049:网络设备状态标识
# UP:网卡处于启动状态
# LOOPBACK:IP数据包回送到本机上,通常用于测试网络配置和本地程序之间通信用
# RUNNING:代表网卡的网线被接上
# MULTICAS:网卡可以发送多播包
# mtu:最大传输单元(这里设置的16384是否以太网设置的？)
lo0: flags=8049<UP,LOOPBACK,RUNNING,MULTICAS> mtu 16384

# 参数? 可以设置值
options=1203<RXCSUM,TXCSUM,TXSTATUS,SW_TIMESTAMP>

# ipv4地址 127.0.0.1 子网掩码 255.0.0.0
inet 127.0.0.1 netmask 0xff000000

inet6 ::1 prefixlen 128

# ipv6地址
inet6 fe80::1%lo0 prefixlen 64 scopeid 0x1

nd6 options=201<PERFORMNUD,DAD>
```

## gif

[参考](https://www.freebsd.org/cgi/man.cgi?gif(4))
```
# software network interface 网络接口
# POINTOPOINT: 允许2台机器点对点直连
# MULTICAS:网卡可以发送多播包
# mtu:最大传输单元(这里设置的1280是否以太网设置的？)
gif0: flags=8010<POINTOPOINT,MULTICAST> mtu 1280
```
## stf
[参考](https://en.wikipedia.org/wiki/6to4)
```
# stf 6to4 tunnel interface 配置隧道
stf0: flags=0<> mtu 1280
```

## en0
```
# en0: 以太网0
# flags=8863:网络状态标识
# BROADCAST:有广播地址，支持发广播包
# SMART:
# RUNNING:代表网卡的网线被接上
# MULTICAS:网卡可以发送多播包
# mtu: 最大传输单元
en0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
ether c4:b3:01:ce:06:11
# ipv4地址 子网掩码 广播地址
inet 192.168.1.11 netmask 0xffffff00 broadcast 192.168.1.255
# 网络媒介类型 (可手动指定)
media: autoselect
# 激活状态
status: active
```
## anpi0
```
flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	options=400<CHANNEL_IO>
	ether 1a:de:55:3e:f9:27
	inet6 fe80::18de:55ff:fe3e:f927%anpi0 prefixlen 64 scopeid 0x6
	nd6 options=201<PERFORMNUD,DAD>
	media: none
	status: inactive
```
## awdl0
[参考](https://stackoverflow.com/questions/19587701/what-is-awdl-apple-wireless-direct-link-and-how-does-it-work)
```
flags=8943<UP,BROADCAST,RUNNING,PROMISC,SIMPLEX,MULTICAST> mtu 1500
	options=400<CHANNEL_IO>
	ether da:d7:bd:3a:4a:22
	inet6 fe80::d8d7:bdff:fe3a:4a22%awdl0 prefixlen 64 scopeid 0xf
	nd6 options=201<PERFORMNUD,DAD>
	media: autoselect
	status: active
```
## ap1
```
flags=8843<UP,BROADCAST,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	options=400<CHANNEL_IO>
	ether fa:4d:89:63:7c:60
	nd6 options=201<PERFORMNUD,DAD>
	media: autoselect
	status: inactive
```
## llw0
```
flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	options=400<CHANNEL_IO>
	ether da:d7:bd:3a:4a:22
	inet6 fe80::d8d7:bdff:fe3a:4a22%llw0 prefixlen 64 scopeid 0x10
	nd6 options=201<PERFORMNUD,DAD>
	media: autoselect
	status: active
```
## bridge
```
# 具体google下桥接知识
bridge0: flags=8822<BROADCAST,SMART,SIMPLEX,MULTICAST> mtu 1500
options=63<RXCSUM,TXCSUM,TSO4,TSO6>
ether 4a:00:07:5c:bd:00
Configuration:
    id 0:0:0:0:0:0 priority 0 hellotime 0 fwddelay 0
    maxage 0 holdcnt 0 proto stp maxaddr 100 timeout 1200
    root id 0:0:0:0:0:0 priority 0 ifcost 0 port 0
    ipfilter disabled flags 0x2
member: en1 flags=3<LEARNING,DISCOVER>
        ifmaxaddr 0 port 8 priority 0 path cost 0
member: en2 flags=3<LEARNING,DISCOVER>
        ifmaxaddr 0 port 9 priority 0 path cost 0
media: <unknown type>
status: inactive
```
## utun0
```
flags=8051<UP,POINTOPOINT,RUNNING,MULTICAST> mtu 1380
	inet6 fe80::dd56:a38b:3d07:65f%utun0 prefixlen 64 scopeid 0x12
	nd6 options=201<PERFORMNUD,DAD>
```