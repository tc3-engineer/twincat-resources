# ADS、数据与工业通信

核验日期：2026-10-17 · 18 项。返回[总目录](README.md)。

| 编号 | 资源 | 主要用途 |
|---|---|---|
| [I01](#i01) | [AdsClient 官方 API（ADS.NET）](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407705867.html) | WPF 通讯层封装、超时与连接健康判断。 |
| [I02](#i02) | [Event driven read with ADS Notifications](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407534859.html) | 避免界面轮询阻塞；处理窗口销毁后的订阅释放与跨线程更新。 |
| [I03](#i03) | [ADS.NET 4.x → 6.x 迁移指南](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407536907.html) | 旧 .NET Framework 上位机迁移到新版 .NET 时核对不兼容点。 |
| [I04](#i04) | [Adding routes — ADS 路由配置](https://infosys.beckhoff.com/content/1033/tc3_system/5211773067.html) | 工程电脑连接 PLC、排查 NetID/IP 和路由配置问题。 |
| [I05](#i05) | [ADS Return Codes](https://infosys.beckhoff.com/content/1033/tf2000_tc3_hmi_server/374277003.html) | 区分目标端口不存在、路由不存在、超时、符号变化与句柄失效。 |
| [I08](#i08) | [Port_xxx.bootdata](https://infosys.beckhoff.com/content/1033/tc3_grundlagen/4291095051.html) | 备份和诊断持久化文件，核对升级后的 Boot 路径。 |
| [I09](#i09) | [Using recipes — PLC 配方管理](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/3273928331.html) | 建立设备参数配方与导入导出流程，区分 Read/Write/Load 的方向。 |
| [I10](#i10) | [Example: Writing/reading of CSV file](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_utilities/35419787.html) | 建立趋势、示教数据和试验记录导出；检查长行截断与多余 CR。 |
| [I11](#i11) | [FB_FileWrite](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_system/30986763.html) | CSV/二进制记录状态机；检测磁盘满等导致的短写。 |
| [I12](#i12) | [TF6100 OPC UA — Overview](https://infosys.beckhoff.com/content/1033/tf6100_tc3_opcua_server/15549180427.html) | PLC 与 MES、SCADA 或第三方上位系统对接选型。 |
| [I13](#i13) | [TF6310 TCP/IP — Samples](https://infosys.beckhoff.com/content/1033/tf6310_tc3_tcpip/84189579.html) | 相机、条码枪和第三方设备 Socket 通讯状态机参考。 |
| [I14](#i14) | [TF6701 MQTT — Samples](https://infosys.beckhoff.com/content/1033/tf6701_tc3_iot_communication_mqtt/3392123147.html) | 设备联网采集、消息队列与云端接口实现。 |
| [I19](#i19) | [PLCopen Guideline on Software Quality Metrics v1.0](https://www.plcopen.org/download_file/force/5378acfc-c952-4d40-ad76-0ae1c008c188/342/) | 为代码评审、技术债治理和模块复杂度评估建立可复查依据。 |
| [I21](#i21) | [Mapping of the OMAC PackML State Diagram to IEC 61131-3](https://www.plcopen.org/download_file/force/91a361c1-b61b-4e8f-a321-ead1d8e92136/342/) | 把设备状态模型转为 PLC 程序结构的概念参考。 |
| [I22](#i22) | [EtherCAT Diagnosis for Users](https://www.ethercat.org/en/downloads/downloads_60F2A51B4B114D8D81C2668AF90B2312.htm) | 现场总线掉站、链路异常及通信错误定位。 |
| [I23](#i23) | [Beckhoff Training offerings 与免费 e-learning](https://www.beckhoff.com/en-us/support/training-offerings/) | 按知识空白选择课程，建立系统学习路径。 |
| [I24](#i24) | [TR3037 Accelerated Troubleshooting 培训大纲](https://www.beckhoff.com/media/downloads/training/baus-training-tr3037-outline-file.pdf) | 用官方课程纲要整理个人现场调试能力检查表。 |
| [I25](#i25) | [TwinCAT and the Modern Software Development Lifecycle](https://www.beckhoff.com/en-en/support/webinars/webinar-detail_688502.html) | 规划团队协作、代码质量和工程发布流程。 |

<a id="i01"></a>
## I01 · AdsClient 官方 API（ADS.NET）

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407705867.html)

同步/异步连接、符号读写、句柄与通知 API；IsConnected 仅说明本地 ADS 端口已打开。

- 用于：WPF 通讯层封装、超时与连接健康判断。
- 来源：Beckhoff 官方；语言：EN；类型：API 手册
- 版本与边界：已核验正文 Assembly 7.0.0；当前 ADS.NET 首页 V7，旧页面标题可能仍标 V6。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i02"></a>
## I02 · Event driven read with ADS Notifications

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407534859.html)

示范异步订阅、取消订阅和通知数据解析，并说明 WPF UI 线程同步。

- 用于：避免界面轮询阻塞；处理窗口销毁后的订阅释放与跨线程更新。
- 来源：Beckhoff 官方；语言：EN；类型：示例文档
- 版本与边界：按安装的 ADS.NET 主版本核对参数和句柄类型。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i03"></a>
## I03 · ADS.NET 4.x → 6.x 迁移指南

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407536907.html)

解释 TcAdsClient 改为 AdsClient、async 调用、uint 句柄和内存接口变化。

- 用于：旧 .NET Framework 上位机迁移到新版 .NET 时核对不兼容点。
- 来源：Beckhoff 官方；语言：EN；类型：迁移指南
- 版本与边界：此页专讲 4.x→6.x，不代表 V7 的全部迁移事项。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i04"></a>
## I04 · Adding routes — ADS 路由配置

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_system/5211773067.html)

说明目标搜索、IP/主机名、路由添加与 Secure ADS 入口。

- 用于：工程电脑连接 PLC、排查 NetID/IP 和路由配置问题。
- 来源：Beckhoff 官方；语言：EN；类型：配置手册
- 版本与边界：不同操作系统及 TwinCAT 版本的安全默认配置不同。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i05"></a>
## I05 · ADS Return Codes

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf2000_tc3_hmi_server/374277003.html)

集中给出全局、路由、设备、实时系统与 Winsock 错误及解释。

- 用于：区分目标端口不存在、路由不存在、超时、符号变化与句柄失效。
- 来源：Beckhoff 官方；语言：EN；类型：错误码索引
- 版本与边界：本链接位于 HMI 手册，但表中是通用 ADS 错误码；结合具体 FB 文档解释。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i08"></a>
## I08 · Port_xxx.bootdata

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_grundlagen/4291095051.html)

说明持久化启动文件的保存位置、创建时机与 .bootdata-old 行为。

- 用于：备份和诊断持久化文件，核对升级后的 Boot 路径。
- 来源：Beckhoff 官方；语言：EN；类型：系统文件说明
- 版本与边界：4026 起 Windows 路径迁至 ProgramData；4024 与早期版本通常在 C:\TwinCAT。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i09"></a>
## I09 · Using recipes — PLC 配方管理

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/3273928331.html)

覆盖配方创建、文件加载、读写与 RecipeManCommands 入口。

- 用于：建立设备参数配方与导入导出流程，区分 Read/Write/Load 的方向。
- 来源：Beckhoff 官方；语言：EN；类型：操作/编程手册
- 版本与边界：需区分 PLC RecipeManagement 与 TwinCAT HMI Recipe 扩展。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i10"></a>
## I10 · Example: Writing/reading of CSV file

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_utilities/35419787.html)

提供 CSV 缓冲读写示例、换行/分隔符规范及文本模式长度限制。

- 用于：建立趋势、示教数据和试验记录导出；检查长行截断与多余 CR。
- 来源：Beckhoff 官方；语言：EN；类型：示例与格式说明
- 版本与边界：TwinCAT 3.1；Tc2_Utilities；文中长行限制对应所列文本读写方式。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i11"></a>
## I11 · FB_FileWrite

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_system/30986763.html)

说明异步文件写入、Busy 期间限制及实际写入长度 cbWrite。

- 用于：CSV/二进制记录状态机；检测磁盘满等导致的短写。
- 来源：Beckhoff 官方；语言：EN；类型：功能块手册
- 版本与边界：TwinCAT 3.1；Tc2_System；需比较 cbWrite 与 cbWriteLen，不能只看 bError。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i12"></a>
## I12 · TF6100 OPC UA — Overview

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf6100_tc3_opcua_server/15549180427.html)

梳理 TwinCAT OPC UA Server、Client 与 Gateway 的组件关系。

- 用于：PLC 与 MES、SCADA 或第三方上位系统对接选型。
- 来源：Beckhoff 官方；语言：EN；类型：产品技术手册
- 版本与边界：TF6100 版本、授权、证书及平台支持需按目标环境核对。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i13"></a>
## I13 · TF6310 TCP/IP — Samples

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf6310_tc3_tcpip/84189579.html)

包含单/多连接 Echo、二进制协议、TLS、UDP 点对点与组播示例。

- 用于：相机、条码枪和第三方设备 Socket 通讯状态机参考。
- 来源：Beckhoff 官方；语言：EN；类型：官方示例索引
- 版本与边界：官方链接指向 Beckhoff/TF6310_Samples；运行需要对应 TF6310 环境。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i14"></a>
## I14 · TF6701 MQTT — Samples

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf6701_tc3_iot_communication_mqtt/3392123147.html)

列出队列/回调、TLS、MQTTv5 请求响应和 JSON/XML 示例。

- 用于：设备联网采集、消息队列与云端接口实现。
- 来源：Beckhoff 官方；语言：EN；类型：官方示例索引
- 版本与边界：官方链接指向 Beckhoff/TF6701_Samples；MQTTv3/v5 FB 与依赖版本需区分。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i19"></a>
## I19 · PLCopen Guideline on Software Quality Metrics v1.0

[打开原始资料](https://www.plcopen.org/download_file/force/5378acfc-c952-4d40-ad76-0ae1c008c188/342/)

给出工业控制软件质量度量的官方指南。

- 用于：为代码评审、技术债治理和模块复杂度评估建立可复查依据。
- 来源：PLCopen 标准组织；语言：EN；类型：PDF 规范
- 版本与边界：2023-11-07，v1.0，65 页。
- 获取/许可：PLCopen 版权所有；公开下载不等于允许再分发；默认收录链接与原创摘要
- 核验：opened，2026-10-17

<a id="i21"></a>
## I21 · Mapping of the OMAC PackML State Diagram to IEC 61131-3

[打开原始资料](https://www.plcopen.org/download_file/force/91a361c1-b61b-4e8f-a321-ead1d8e92136/342/)

说明 PackML 状态图到 IEC 61131-3 的映射思路。

- 用于：把设备状态模型转为 PLC 程序结构的概念参考。
- 来源：PLCopen 标准组织；语言：EN；类型：PDF 技术说明
- 版本与边界：4 页历史技术说明；最新 PackML 状态与接口语义应以适用版本标准为准。
- 获取/许可：PLCopen 版权所有；公开下载不等于允许再分发；默认收录链接与原创摘要
- 核验：opened，2026-10-17

<a id="i22"></a>
## I22 · EtherCAT Diagnosis for Users

[打开原始资料](https://www.ethercat.org/en/downloads/downloads_60F2A51B4B114D8D81C2668AF90B2312.htm)

涵盖诊断能力、硬件/软件故障与典型排查顺序。

- 用于：现场总线掉站、链路异常及通信错误定位。
- 来源：EtherCAT Technology Group 官方；语言：EN；类型：诊断指南/PDF 入口
- 版本与边界：2018-11-09；官方索引显示有多语言版本；本次直接打开遇到 403，搜索索引核验。
- 获取/许可：ETG 版权所有；再分发授权未确认；仅收录链接与原创摘要
- 核验：search_result，2026-10-17

<a id="i23"></a>
## I23 · Beckhoff Training offerings 与免费 e-learning

[打开原始资料](https://www.beckhoff.com/en-us/support/training-offerings/)

提供官方在线自学入口和 PLC、运动、诊断等培训目录。

- 用于：按知识空白选择课程，建立系统学习路径。
- 来源：Beckhoff 官方；语言：EN；类型：课程目录
- 版本与边界：美国站；免费 e-learning 需注册，课堂/专项培训另行确认条件。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i24"></a>
## I24 · TR3037 Accelerated Troubleshooting 培训大纲

[打开原始资料](https://www.beckhoff.com/media/downloads/training/baus-training-tr3037-outline-file.pdf)

列出 Runtime、EtherCAT、TwinSAFE、NC PTP、I/O、PLC 故障诊断和备份主题。

- 用于：用官方课程纲要整理个人现场调试能力检查表。
- 来源：Beckhoff 官方；语言：EN；类型：PDF 培训大纲
- 版本与边界：2025-10-22，5 页；这是培训大纲，并非完整教材。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17

<a id="i25"></a>
## I25 · TwinCAT and the Modern Software Development Lifecycle

[打开原始资料](https://www.beckhoff.com/en-en/support/webinars/webinar-detail_688502.html)

介绍版本控制、自动化测试、持续集成在 TwinCAT 工程中的应用。

- 用于：规划团队协作、代码质量和工程发布流程。
- 来源：Beckhoff 官方；语言：EN；类型：官方 Webinar
- 版本与边界：2024-10-09 视频；工具界面和版本依赖需参照当前文档。
- 获取/许可：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- 核验：opened，2026-10-17
