
# 通用工具

## git
分布式版本控制平台
- 初始化仓库： git init 
- 添加文件： git add <文件>  或  git add . （全部添加）
- 提交更改： git commit -m "提交说明" 
- 分支管理： git branch <分支名> （创建）， git checkout <分支名> （切换）
- 远程同步： git remote add origin <仓库URL> ， git push -u origin <分支> 
## docker
容器化平台
- 拉取镜像： docker pull <镜像名> （如  docker pull ubuntu ）
- 运行容器： docker run -it <镜像名> （交互式）， docker run -d <镜像名> （后台运行）
- 管理容器： docker ps （查看运行中）， docker stop <容器ID> （停止）， docker rm <容器ID> （删除）
- 构建镜像：编写  Dockerfile  后， docker build -t <镜像名> 
## GDB
调试工具
- 启动调试： gdb <可执行程序> 
- 断点设置： break <行号/函数名> 
- 执行控制： run （运行）， next （单步跳过函数）， step （单步进入函数）
- 查看信息： print <变量> （查看值）， backtrace （查看堆栈）

## IDA Pro
逆向工程工具
- 加载文件：拖入二进制文件（.exe、.so等），IDA自动分析。
- 反汇编视图：查看  IDA View  窗口， F5 （需Hex-Rays插件）生成伪代码。
- 代码分析：使用交叉引用（ X  键）、重命名符号（ N  键）优化可读性，利用插件（如反混淆）扩展功能。

## Wireshark
网络协议分析工具
- 捕获数据包：选择网卡，点击“开始”，分析实时流量。
- 过滤规则：输入  tcp.port == 80 （HTTP流量）等条件筛选。
- 协议解析：展开数据包，查看链路层、IP、TCP/UDP、应用层（如HTTP、DNS）详情。
- 导出数据：保存为  .pcap  文件，用于离线分析。

## Burp Suite
Web安全测试工具
- 代理配置：浏览器设为  127.0.0.1:8080 ，Burp监听代理流量。
- 目标扫描： Spider  爬取站点， Scanner  自动检测漏洞（如SQL注入、XSS）。
- 请求拦截： Proxy  模块拦截HTTP请求，修改后放行（测试输入验证）。
- 暴力测试： Intruder  模块进行字典攻击（如密码爆破）， Repeater  手动重放请求。
# 贡献指南

参考 [链接](https://github.com/OpenHUTB/.github/blob/master/CONTRIBUTING.md) 。
