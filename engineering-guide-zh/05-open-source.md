# 开源项目与工具

核验日期：2026-10-17 · 20 项。返回[总目录](README.md)。

| 编号 | 资源 | 主要用途 |
|---|---|---|
| [O01](#o01) | [TcUnit 单元测试框架](https://github.com/tcunit/TcUnit) | 给状态迁移、凸轮点计算、模拟量换算、配方检查建立可重复测试。 |
| [O02](#o02) | [TcUnit-Runner（归档）](https://github.com/tcunit/TcUnit-Runner) | 研究从 Git 提交到 PLC 测试结果的自动化链路。 |
| [O03](#o03) | [TcOpen 原始社区版（归档）](https://github.com/TcOpenGroup/TcOpen) | 研究模块层级、统一任务握手、气缸轴对象与协调器的职责边界。 |
| [O04](#o04) | [TcOpen Inxton 维护入口](https://github.com/Inxton/TcOpen) | 研究大型设备的组件组合、异步动作与上位机映射。 |
| [O05](#o05) | [TcLog](https://github.com/bengeisler/TcLog) | 给启动/暂停/复位、真空交接和偶发卡步记录带上下文的事件。 |
| [O06](#o06) | [log4TC](https://github.com/mbc-engineering/log4TC) | 离线追溯偶发故障及流程顺序，跨多控制器汇集事件。 |
| [O07](#o07) | [TcStaticAnalysisLoader](https://github.com/sagatowski/TcStaticAnalysisLoader) | 将未使用变量、代码规则等检查接入工程构建流程。 |
| [O08](#o08) | [TcBuild（JustusRijke）](https://github.com/JustusRijke/TcBuild) | 先实现本地一键编译、收集编译告警，再接 CI。 |
| [O09](#o09) | [mobject-core](https://github.com/Mobject-Dev-Team/mobject-core) | 研究接口、集合、对象组合及可复用基础设施的实现。 |
| [O10](#o10) | [Beckhoff ADS / AdsLib](https://github.com/Beckhoff/ADS) | 理解 ADS 路由、协议读写与错误链，建设独立通信诊断工具。 |
| [O11](#o11) | [Beckhoff ADS .NET V6 示例](https://github.com/Beckhoff/TF6000_ADS_DOTNET_V5_Samples) | 作为 WPF/ADS 通信、符号访问、通知与异步调用的权威起点。 |
| [O12](#o12) | [pyads](https://github.com/stlehmann/pyads) | 写参数快照、配方比对、调试数据采集与自动回归脚本。 |
| [O13](#o13) | [ads-client](https://github.com/jisotalo/ads-client) | 构建轻量诊断页面或 Node-RED 调试流，研究订阅重连和批量请求。 |
| [O14](#o14) | [Twingrind](https://github.com/stefanbesler/twingrind) | 定位偶发周期超时、重计算和复杂 FB 调用链耗时。 |
| [O15](#o15) | [Twinpack](https://github.com/Zeugwerk/Twinpack) | 固化工程库版本，减少不同电脑上引用版本飘移。 |
| [O16](#o16) | [TcBlack](https://github.com/Roald87/TcBlack) | 减少格式噪声，让 Git diff 聚焦逻辑更改。 |
| [O17](#o17) | [SPT-Libraries](https://github.com/Beckhoff-USA-Community/SPT-Libraries) | 优先学习整机模式、设备模块、轴/气缸对象和报警层次。 |
| [O18](#o18) | [SPT V4 Samples](https://github.com/Beckhoff-USA-Community/SPT_V4_Samples) | 对照叠片机的模式切换、凸轮耦合、报警以及停止恢复设计。 |
| [O19](#o19) | [PackML PLC Example / VFFS Demo](https://github.com/Beckhoff-USA-Community/PackML_PLC_Example) | 借鉴完整机器层与模块层的连接方式、状态流转及调试入口。 |
| [O20](#o20) | [PLC Sphinx Parser / plcdoc](https://github.com/DEMCON/plcdoc) | 研究让接口、FB、函数说明跟随源码生成的方案。 |

<a id="o01"></a>
## O01 · TcUnit 单元测试框架

[打开原始资料](https://github.com/tcunit/TcUnit)

xUnit 风格断言、测试套件与 TwinCAT 内测试。

- 用于：给状态迁移、凸轮点计算、模拟量换算、配方检查建立可重复测试。
- 来源：项目原作者 tcunit / Jakob Sagatowski；语言：ST、C#；英文文档；类型：PLC 库
- 版本与边界：README 标记 stable but resting；目前不积极开发，issue/PR 可能无人处理，不代表功能失效。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/tcunit/TcUnit/blob/master/LICENSE)

<a id="o02"></a>
## O02 · TcUnit-Runner（归档）

[打开原始资料](https://github.com/tcunit/TcUnit-Runner)

自动执行 TcUnit 并导出 xUnit/JUnit XML。

- 用于：研究从 Git 提交到 PLC 测试结果的自动化链路。
- 来源：项目原作者 tcunit / Jakob Sagatowski；语言：C#；英文文档；类型：CI 测试运行器
- 版本与边界：2025-10-17 已归档；README 使用 VS2013、ADS .NET 4.4.19 等旧依赖，仅作历史实现参考。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/tcunit/TcUnit-Runner/blob/master/LICENSE)

<a id="o03"></a>
## O03 · TcOpen 原始社区版（归档）

[打开原始资料](https://github.com/TcOpenGroup/TcOpen)

面向对象的任务、组件、顺序协调、报警、日志及 .NET 数据交互。

- 用于：研究模块层级、统一任务握手、气缸轴对象与协调器的职责边界。
- 来源：项目原作者 TcOpenGroup；语言：ST、C#；英文文档；类型：应用框架
- 版本与边界：2025-03-25 归档；以历史代码研究为主，和 Inxton 后续仓库区分；IVF 依赖另查许可。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/TcOpenGroup/TcOpen/blob/dev/LICENSE)

<a id="o04"></a>
## O04 · TcOpen Inxton 维护入口

[打开原始资料](https://github.com/Inxton/TcOpen)

包含消息、顺序协调、检查器、气缸、NC 驱动及 PLC/.NET 数据框架。

- 用于：研究大型设备的组件组合、异步动作与上位机映射。
- 来源：Inxton 官方项目团队；语言：ST、C#；英文文档；类型：应用框架
- 版本与边界：README 明确仅按 Inxton 内部需求维护、无继续扩展计划且不接受贡献；先决条件列 4024.17+、VS2019、.NET 4.8/.NET6，须自行验证现用环境。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Inxton/TcOpen/blob/dev/LICENSE)

<a id="o05"></a>
## O05 · TcLog

[打开原始资料](https://github.com/bengeisler/TcLog)

纯 PLC 库提供 ADS 输出、文件日志、级别过滤、滚动文件与缓冲。

- 用于：给启动/暂停/复位、真空交接和偶发卡步记录带上下文的事件。
- 来源：原作者 Benedikt Geisler；语言：ST；英文文档；类型：PLC 日志库
- 版本与边界：仓库包含 TcUnit 与 .NET 集成测试；测试版依赖和正式库生成流程不同，需按安装说明选版本。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/bengeisler/TcLog/blob/main/LICENSE)

<a id="o06"></a>
## O06 · log4TC

[打开原始资料](https://github.com/mbc-engineering/log4TC)

PLC 日志通过服务处理、过滤并写入多种输出，支持结构化日志。

- 用于：离线追溯偶发故障及流程顺序，跨多控制器汇集事件。
- 来源：原作者 mbc engineering；语言：ST、C#；英文文档；类型：日志库与 Windows 服务
- 版本与边界：代码仓库 Apache-2.0；当前 README 同时描述商用成品试用与授权，预编译发行包条款需独立核对；依赖 Windows 服务。
- 获取/许可：Apache-2.0
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/mbc-engineering/log4TC/blob/master/LICENSE)

<a id="o07"></a>
## O07 · TcStaticAnalysisLoader

[打开原始资料](https://github.com/sagatowski/TcStaticAnalysisLoader)

配合 AllTwinCAT CI/CD 系列运行 TwinCAT 静态代码分析。

- 用于：将未使用变量、代码规则等检查接入工程构建流程。
- 来源：原作者 Jakob Sagatowski；语言：C#；英文文档；类型：静态分析自动化示例
- 版本与边界：README 要求结合其四篇 CI/CD 教程；属于示例实现，不等于现版本 TwinCAT 静态分析产品本体，工程环境及授权须匹配。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/sagatowski/TcStaticAnalysisLoader/blob/master/LICENSE)

<a id="o08"></a>
## O08 · TcBuild（JustusRijke）

[打开原始资料](https://github.com/JustusRijke/TcBuild)

命令行构建 TwinCAT 解决方案并保存/安装 PLC 库，返回分级退出码。

- 用于：先实现本地一键编译、收集编译告警，再接 CI。
- 来源：原作者 JustusRijke；语言：C#；英文文档；类型：命令行构建工具
- 版本与边界：README 要求 Windows 10 x64、.NET Framework4.8+、独立安装 TwinCAT4024+；明确未测试 VS 集成安装，且其他作者存在同名工具。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/JustusRijke/TcBuild/blob/main/LICENSE)

<a id="o09"></a>
## O09 · mobject-core

[打开原始资料](https://github.com/Mobject-Dev-Team/mobject-core)

以类与接口补充 TwinCAT 面向对象开发的基础能力。

- 用于：研究接口、集合、对象组合及可复用基础设施的实现。
- 来源：项目原作者 Mobject Development Team；语言：ST；英文文档；类型：OOP 基础库
- 版本与边界：项目组织明确标注 alpha 并劝阻生产使用；仓库安装说明针对 4024。适合学习和隔离验证，不能直接作为成熟整机框架保证。
- 获取/许可：MIT；另含 TcUnit MIT 通知
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Mobject-Dev-Team/mobject-core/blob/main/LICENSE)

<a id="o10"></a>
## O10 · Beckhoff ADS / AdsLib

[打开原始资料](https://github.com/Beckhoff/ADS)

官方 ADS 客户端库、AdsTool、测试工程及跨平台编译示例。

- 用于：理解 ADS 路由、协议读写与错误链，建设独立通信诊断工具。
- 来源：Beckhoff 官方；语言：C++；英文文档；类型：协议客户端与工具
- 版本与边界：当前 README 要求 C++14，列多种 Linux/BSD/Windows 交叉编译测试环境；其定位主要是非 Windows ADS 客户端。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Beckhoff/ADS/blob/master/LICENSE)

<a id="o11"></a>
## O11 · Beckhoff ADS .NET V6 示例

[打开原始资料](https://github.com/Beckhoff/TF6000_ADS_DOTNET_V5_Samples)

ADS .NET API 的官方示例集合。

- 用于：作为 WPF/ADS 通信、符号访问、通知与异步调用的权威起点。
- 来源：Beckhoff 官方；语言：C#；英文文档；类型：官方示例工程
- 版本与边界：仓库名仍含 V5，当前 README 明确面向 Version6.X；使用前对齐 NuGet 主版本与目标运行环境。
- 获取/许可：0BSD
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Beckhoff/TF6000_ADS_DOTNET_V5_Samples/blob/main/LICENSE.md)

<a id="o12"></a>
## O12 · pyads

[打开原始资料](https://github.com/stlehmann/pyads)

Python 对 ADS API 的封装，支持变量、结构体及通知。

- 用于：写参数快照、配方比对、调试数据采集与自动回归脚本。
- 来源：原作者 Stefan Lehmann 与维护者；语言：Python；英文文档；类型：ADS 客户端库
- 版本与边界：支持 TwinCAT2/3；Windows 用 TcAdsDll、Linux 用 AdsLib；README 说明是业余维护项目，响应速度不保证。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/stlehmann/pyads/blob/master/LICENSE)

<a id="o13"></a>
## O13 · ads-client

[打开原始资料](https://github.com/jisotalo/ads-client)

Node.js ADS 客户端，含订阅、RPC、SumCommands 与连接排障说明。

- 用于：构建轻量诊断页面或 Node-RED 调试流，研究订阅重连和批量请求。
- 来源：原作者 Jussi Isotalo；语言：TypeScript、JavaScript；英文文档；类型：ADS 客户端库
- 版本与边界：README 标记 2024-12-14 发布 v2 并用 TypeScript 重写；有 MIGRATION.md，旧 v1 代码需检查迁移差异；非官方库。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/jisotalo/ads-client/blob/master/LICENSE.txt)

<a id="o14"></a>
## O14 · Twingrind

[打开原始资料](https://github.com/stefanbesler/twingrind)

PLC 插桩采集调用栈并导出 Callgrind 数据分析慢周期。

- 用于：定位偶发周期超时、重计算和复杂 FB 调用链耗时。
- 来源：原作者 Stefan Besler；语言：ST、Python；英文文档；类型：调用图性能分析工具
- 版本与边界：README 限制为一个 PLC 任务及 ST 实现；插桩会修改源码并增加执行开销，不支持混合非 ST 实现。
- 获取/许可：GPL-3.0
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/stefanbesler/twingrind/blob/main/LICENSE)

<a id="o15"></a>
## O15 · Twinpack

[打开原始资料](https://github.com/Zeugwerk/Twinpack)

集成 TwinCAT IDE 的 PLC 库管理器，支持 Twinpack、NuGet、Beckhoff4026库源。

- 用于：固化工程库版本，减少不同电脑上引用版本飘移。
- 来源：原作者 Zeugwerk；语言：C#；英文文档；类型：库包管理工具
- 版本与边界：不是 Beckhoff TwinCAT Package Manager；README 指其可安装任意发布者 PLC 库，软件和包内库各自遵循各自许可。
- 获取/许可：GPL-3.0
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Zeugwerk/Twinpack/blob/main/LICENSE)

<a id="o16"></a>
## O16 · TcBlack

[打开原始资料](https://github.com/Roald87/TcBlack)

提供 CLI 和 Visual Studio 扩展统一 TwinCAT 代码格式。

- 用于：减少格式噪声，让 Git diff 聚焦逻辑更改。
- 来源：原作者 Roald Ruiter；语言：C#；英文文档；类型：ST 格式化工具
- 版本与边界：README 明确为 alpha，要求仅对已纳入版本控制的文件使用；适合独立分支小范围验证。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Roald87/TcBlack/blob/master/LICENSE)

<a id="o17"></a>
## O17 · SPT-Libraries

[打开原始资料](https://github.com/Beckhoff-USA-Community/SPT-Libraries)

面向机器程序架构的 SPT 框架及 PackML 配套库。

- 用于：优先学习整机模式、设备模块、轴/气缸对象和报警层次。
- 来源：Beckhoff 美国团队示例项目；语言：ST；英文文档；类型：设备框架库
- 版本与边界：当前 README 宣布 V4 对应 TwinCAT3.1.4026 的 PackML V3；旧 V3 工程需先固定库版本，不能直接混换。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Beckhoff-USA-Community/SPT-Libraries/blob/main/LICENSE)

<a id="o18"></a>
## O18 · SPT V4 Samples

[打开原始资料](https://github.com/Beckhoff-USA-Community/SPT_V4_Samples)

含 EtherCAT 诊断、凸轮、回零、受控停止、模式管理及多主轴示例。

- 用于：对照叠片机的模式切换、凸轮耦合、报警以及停止恢复设计。
- 来源：Beckhoff 美国团队示例项目；语言：ST；英文文档；类型：框架示例集合
- 版本与边界：按子工程核对 SPT V4 与 PackML 依赖；README 仍有模板占位说明，其通用最低版本描述不能替代子工程实际依赖。
- 获取/许可：0BSD
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Beckhoff-USA-Community/SPT_V4_Samples/blob/main/LICENSE)

<a id="o19"></a>
## O19 · PackML PLC Example / VFFS Demo

[打开原始资料](https://github.com/Beckhoff-USA-Community/PackML_PLC_Example)

展示如何以 PackML 基础框架组织一台立式包装机程序，含说明 PDF。

- 用于：借鉴完整机器层与模块层的连接方式、状态流转及调试入口。
- 来源：Beckhoff 美国团队示例项目；语言：ST；英文文档；类型：完整机器示例
- 版本与边界：当前 README 明确要求 SPT-Libraries V3.9；与 SPT V4 示例分开看。
- 获取/许可：MIT
- 核验：opened，2026-10-17
- [上游许可证](https://github.com/Beckhoff-USA-Community/PackML_PLC_Example/blob/main/LICENSE)

<a id="o20"></a>
## O20 · PLC Sphinx Parser / plcdoc

[打开原始资料](https://github.com/DEMCON/plcdoc)

解析 TwinCAT ST 声明与注释，生成 Sphinx 文档。

- 用于：研究让接口、FB、函数说明跟随源码生成的方案。
- 来源：原作者 DEMCON；语言：Python；英文文档；类型：文档生成工具
- 版本与边界：README 标明 work-in-progress，并提示可能有较多告警/错误；本次未在仓库根目录及 README 确认明确许可证。
- 获取/许可：未确认；仅收录链接
- 核验：opened，2026-10-17
