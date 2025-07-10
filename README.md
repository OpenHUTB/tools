
# 通用工具

## git
Git 是分布式版本控制系统，工作目录、暂存区、本地仓库是核心区域。工作目录存放项目文件，文件有未跟踪、已修改状态；暂存区临时存放待提交修改；本地仓库存储版本历史，记录提交、分支等信息 。通过  git add  关联工作目录与暂存区， git commit  关联暂存区与本地仓库，实现版本管理
## docker
Docker 中，镜像（Image）是只读模板，包含运行程序的环境与代码；容器（Container）是镜像运行实例，可启动、停止、删除；仓库（Repository）存储镜像，分公共（如 Docker Hub ）、私有 。通过  docker pull  拉取镜像， docker run  基于镜像创建容器， docker push  推送镜像到仓库，实现应用打包、分发、运行 。

## GDB
调试工具
启动调试： gdb <可执行程序> 
断点设置： break <行号/函数名> 
执行控制： run （运行）， next （单步跳过函数）， step （单步进入函数）
查看信息： print <变量> （查看值）， backtrace （查看堆栈）

## IDA Pro
IDA Pro 是逆向工程核心工具，融合静态分析与动态调试。静态分析通过 Hex View（原始字节码）、Disassembly View（反汇编代码）、Graph View（函数控制流图）解析二进制文件，F5 生成伪 C 代码辅助逻辑理解，交叉引用（X 键）追踪函数调用与数据流向；符号识别（N 键重命名）提升代码可读性。动态调试依托 Remote Linux/Windows Debugger，F2 设断点、Run to cursor 控制执行，结合 Registers（寄存器）、Memory（内存）、Stack（栈）窗口分析运行状态，Patch Program 可修改二进制绕过反调试。综合运用 Flirt 技术（识别库函数）、Decompiler 插件（还原混淆代码），完整还原程序逻辑，支撑安全分析。

## Wireshark
网络协议分析工具
捕获数据包：选择网卡，点击“开始”，分析实时流量。
过滤规则：输入  tcp.port == 80 （HTTP流量）等条件筛选。
协议解析：展开数据包，查看链路层、IP、TCP/UDP、应用层（如HTTP、DNS）详情。
导出数据：保存为  .pcap  文件，用于离线分析。

## Burp Suite
Web安全测试工具
代理配置：浏览器设为  127.0.0.1:8080 ，Burp监听代理流量。
目标扫描： Spider  爬取站点， Scanner  自动检测漏洞（如SQL注入、XSS）。
请求拦截： Proxy  模块拦截HTTP请求，修改后放行（测试输入验证）。
暴力测试： Intruder  模块进行字典攻击（如密码爆破）， Repeater  手动重放请求。
# 贡献指南

参考 [链接](https://github.com/OpenHUTB/.github/blob/master/CONTRIBUTING.md) 。
