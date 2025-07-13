
# 通用工具

## git


## docker


## docker  
Docker 中，镜像（Image）可看作 “带运行环境的二进制包”，若镜像运行异常，可像逆向分析程序一样：用 ‘docker export’ 导出容器文件系统，拖进 IDA Pro 分析二进制依赖；容器（Container）是**“动态调试沙箱”，启动时加 ‘--cap-add=SYS_PTRACE’ ，就能用 GDB  attach 进容器进程（比如调试加密程序的内存行为）；仓库（Repository）存储的镜像，可通过 ‘docker save`’导出后，用 Binwalk 拆解镜像层 ，逆向工程师能快速定位“恶意镜像藏了什么脚本”。  

实战里，‘docker pull’下载可疑镜像后，先在隔离环境 ‘docker run’，结合 Wireshark 抓容器网络包（看是否外联恶意地址）；分析完用 ‘docker rmi’ 彻底删除，这种 “Docker + 逆向工具链” 的组合 ，让镜像安全审计更高效，也让 Docker 不止于部署，成为逆向分析的 “动态靶场” 。  



## GDB
调试工具
启动调试： gdb <可执行程序> 
断点设置： break <行号/函数名> 
执行控制： run （运行）， next （单步跳过函数）， step （单步进入函数）
查看信息： print <变量> （查看值）， backtrace （查看堆栈）


## IDA Pro


## Wireshark
Wireshark 是一款常用的网络协议分析工具，其基本原理涉及数据捕获、数据解析、数据显示这几个关键环节。数据捕获，Wireshark 在进行数据捕获时，会将网卡设置为混杂模式，使其能接收流经该网卡的所有数据包，不管这些数据包的目的地址是不是本机。这样就能获取到网络中传输的所有数据流量。数据解析，Wireshark 内置了大量的协议解析器，涵盖了 TCP/IP 协议族、应用层协议，以及其他众多网络协议。当捕获到原始数据包后，Wireshark 会根据数据包的头部特征，按照从链路层到应用层的顺序，依次将数据包与各个协议解析器进行匹配。依据网络分层模型，Wireshark 对数据包进行层次化解析。先解析链路层，接着解析网络层，再解析传输层，最后解析应用层协议，提取出具体的应用数据。
数据显示，Wireshark 提供了一个直观的图形用户界面，将解析后的数据以表格形式呈现。为了便于用户快速识别不同类型的数据包，Wireshark 还支持颜色编码功能。

## Burp Suite

# 贡献指南

参考 [链接](https://github.com/OpenHUTB/.github/blob/master/CONTRIBUTING.md) 。
