
# 通用工具

## git
 
Git 是分布式版本控制系统，工作目录、暂存区、本地仓库是核心区域。工作目录存放项目文件，文件有未跟踪、已修改状态；暂存区临时存放待提交修改；本地仓库存储版本历史，记录提交、分支等信息 。通过  git add  关联工作目录与暂存区， git commit  关联暂存区与本地仓库，实现版本管理

## docker
Docker 中，镜像（Image）是只读模板，包含运行程序的环境与代码；容器（Container）是镜像运行实例，可启动、停止、删除；仓库（Repository）存储镜像，分公共（如 Docker Hub ）、私有 。通过  docker pull  拉取镜像， docker run  基于镜像创建容器， docker push  推送镜像到仓库，实现应用打包、分发、运行 。
## GDB

## IDA Pro
IDA Pro 是逆向工程核心工具，融合静态分析与动态调试。静态分析通过 Hex View（原始字节码）、Disassembly View（反汇编代码）、Graph View（函数控制流图）解析二进制文件，F5 生成伪 C 代码辅助逻辑理解，交叉引用（X 键）追踪函数调用与数据流向；符号识别（N 键重命名）提升代码可读性。动态调试依托 Remote Linux/Windows Debugger，F2 设断点、Run to cursor 控制执行，结合 Registers（寄存器）、Memory（内存）、Stack（栈）窗口分析运行状态，Patch Program 可修改二进制绕过反调试。综合运用 Flirt 技术（识别库函数）、Decompiler 插件（还原混淆代码），完整还原程序逻辑，支撑安全分析。


## Wireshark
Wireshark 是一款常用的网络协议分析工具，其基本原理涉及数据捕获、数据解析、数据显示这几个关键环节。数据捕获，Wireshark 在进行数据捕获时，会将网卡设置为混杂模式，使其能接收流经该网卡的所有数据包，不管这些数据包的目的地址是不是本机。这样就能获取到网络中传输的所有数据流量。数据解析，Wireshark 内置了大量的协议解析器，涵盖了 TCP/IP 协议族、应用层协议，以及其他众多网络协议。当捕获到原始数据包后，Wireshark 会根据数据包的头部特征，按照从链路层到应用层的顺序，依次将数据包与各个协议解析器进行匹配。依据网络分层模型，Wireshark 对数据包进行层次化解析。先解析链路层，接着解析网络层，再解析传输层，最后解析应用层协议，提取出具体的应用数据。
数据显示，Wireshark 提供了一个直观的图形用户界面，将解析后的数据以表格形式呈现。为了便于用户快速识别不同类型的数据包，Wireshark 还支持颜色编码功能。

## Burp Suite

# 贡献指南

参考 [链接](https://github.com/OpenHUTB/.github/blob/master/CONTRIBUTING.md) 。
