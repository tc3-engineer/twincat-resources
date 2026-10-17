# TwinCAT 3 PLC 编程与调试 · 中文工程资源库

核验日期：**2026-10-17**。收录 **137 项去重资源**，优先厂商/标准组织官方文档和作者原始项目。每项说明用途、来源、版本限制、获取方式和核验状态。

这是一份面向设备编程与现场调试的范围化汇编；不是“互联网上所有倍福资料已经收齐”的声明。打开网页表示资料页可核实，不代表视频已逐集观看、附件全部下载或工程编译通过。

## 从哪里开始

- 找现有故障：读 [现场问题索引与工程实践](FIELD_GUIDE.md)。
- 搭建可维护架构：先读 [架构与规范](01-architecture.md)，再比较官方示例、State Pattern 与 PackML。
- 查具体资料：打开对应分类，或下载 [catalog.html](catalog.html) 后在浏览器离线搜索。
- 想获取可读源码：看 [源码与官方下载说明](DOWNLOADS.md)；10 个项目已固定版本。
- 按顺序学习：看 [六阶段学习路线](LEARNING_PATH.md)。

## 分类目录

| 分类 | 去重条目 | 主要内容 |
|---|---:|---|
| [架构与规范](01-architecture.md) | 27 | OOP、状态机、单写者、生命周期、PackML、PLCopen规范 |
| [运动控制与凸轮](02-motion.md) | 25 | PLCopen调用、耦合、模轴、凸轮、动态校核、伺服整定 |
| [现场诊断与测量](03-diagnostics.md) | 31 | 任务超周期、启动、core dump、Scope、EtherCAT、Wireshark |
| [ADS、数据与工业通信](04-integration.md) | 18 | ADS/WPF、通知、配方、持久化、CSV、TCP、OPC UA、MQTT |
| [开源项目与工具](05-open-source.md) | 20 | 单元测试、日志、构建、静态分析、格式化、架构源码 |
| [版本、PID与学习入口](06-engineering.md) | 16 | 4024/4026、PID、性能工具、仿真、中文官方入口 |

跨分类的相同原始 URL 只计一次。全部资源和检索字段在 [data/catalog.json](data/catalog.json)，重复编号映射在 [data/id-aliases.json](data/id-aliases.json)。

## 使用前最值得先看的版本差异

- 新凸轮库有最低运行时要求，查 [M10](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/6961172235.html)，不能仅因库可安装就认定旧 XAR 可运行。
- TE1210 PLC Profiler 最低 4026，查 [R15](https://infosys.beckhoff.com/content/1033/te1210_tc3_plcprofiler/16451977355.html?id=1577261788004725561)；它自身会影响负载。
- 当前 SPT V4 与旧 PackML 例程所需依赖不同，查 [O17](https://github.com/Beckhoff-USA-Community/SPT-Libraries)、[O19](https://github.com/Beckhoff-USA-Community/PackML_PLC_Example)。
- ADS.NET 当前文档与样例仓库可能属于不同主版本，查 [I01](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407705867.html)、[O11](https://github.com/Beckhoff/TF6000_ADS_DOTNET_V5_Samples)。
- 不要把厂商新版本的 Online Change、指针恢复和启动选项直接套到旧环境，查 [D05](https://infosys.beckhoff.com/content/1033/tc3_userinterface/3434442123.html)、[D08](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2531444363.html)。

## 来源与归档规则

官方资料负责产品接口和限制；作者文章负责其自身实现思路。社区项目不是 Beckhoff 全产品认证。所有工程仍需按照本地库声明、版本、目标架构与现场条件验证。

保存的是原创中文索引、实践整理、官方入口及带许可证的固定源码引用。官方手册、付费课程、未确认许可的文章与工程仅链接；公开可读不等于可全文转载。原有仓库首页与许可证保留。

[检索范围与完成标准](COVERAGE.md) · [维护方法](MAINTENANCE.md) · [第三方许可说明](THIRD_PARTY_NOTICES.md)
