# 现场诊断与测量

核验日期：2026-10-17 · 31 项。返回[总目录](README.md)。

| 编号 | 资源 | 主要用途 |
|---|---|---|
| [D01](#d01) | [Real-Time：调度、任务超周期与 I/O 更新时间](https://infosys.beckhoff.com/content/1033/tc3_grundlagen/6828869003.html) | 高速设备节拍不稳定时，区分任务运算超时、输出更新时间波动及跨任务延迟。 |
| [D02](#d02) | [Real-Time Online：CPU 负载与系统延迟](https://infosys.beckhoff.com/content/1033/tc3_system/5206501899.html) | 程序运行前后对比负载和延迟，建立可复现的性能基线。 |
| [D03](#d03) | [FB_ReadTaskExceedCounter：读取任务超周期计数](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_system/11267603979.html) | 将超周期计数纳入设备诊断；验证大循环、文件处理或批量数据计算是否造成超时。 |
| [D04](#d04) | [Project tab：PLC Boot Project 自启动](https://infosys.beckhoff.com/content/1033/tc3_userinterface/3434440203.html) | 换 PLC、还原工程后，检查为何 TwinCAT 已 RUN 而 PLC 未自动启动。 |
| [D05](#d05) | [PLC Settings：启动超时、Boot 更新与持久化备份](https://infosys.beckhoff.com/content/1033/tc3_userinterface/3434442123.html) | 断电重启异常、旧 bootdata 回读、Online Change 后重启程序回退时查此页。 |
| [D06](#d06) | [Remanent Variables：PERSISTENT 与 RETAIN](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2528803467.html) | 配方、计数器和设备标定数据断电丢失或重启恢复旧值时，核对保存机制。 |
| [D07](#d07) | [FB_WritePersistentData：显式保存持久数据](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_utilities/35030155.html) | 配方变更后受控保存，记录 Busy/ERR/ERRID；避免把周期调用等同于每周期保存。 |
| [D08](#d08) | [Command Online Change：在线修改边界](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2531444363.html) | 修改 FB、接口或隐式检查前评估是否能在线修改，避免误把保留状态当重新初始化。 |
| [D09](#d09) | [FB_init / FB_reinit / FB_exit：生命周期与异常](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/5044757003.html) | 定位激活/启动阶段崩溃，检查初始化代码、引用和指针；避免随意显式调用生命周期方法。 |
| [D10](#d10) | [Error analysis with core dump：离线崩溃定位](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/6884133515.html) | 现场偶发崩溃时一起归档 .core、工程和 .compileinfo，保留可离线分析的证据。 |
| [D11](#d11) | [Flow Control：观察执行位置上的实际值](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527642507.html) | 追踪同一扫描中变量先后赋值、条件命中、流程跳步等问题。 |
| [D12](#d12) | [Use of breakpoints：条件断点和执行点](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527568011.html) | 离线/可控工况定位罕见分支；用条件执行点辅助计数。 |
| [D13](#d13) | [Using Watchlists：集中监视变量](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527704459.html) | 为一个故障集中保存请求、许可、状态、步号、Done/Error 与联锁变量。 |
| [D14](#d14) | [EventLogger Technical introduction：消息与报警模型](https://infosys.beckhoff.com/content/1033/tc3_eventlogger/4278578443.html?id=2759979561564329345) | 建立模块化报警来源和首故障记录，减少只看当前报警而丢失前因的问题。 |
| [D15](#d15) | [EventLogger PLC Tutorial：首个事件](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_eventlogger/4279107979.html) | 把现有模块故障码逐步接入统一事件记录，不必一次重构全机。 |
| [D16](#d16) | [创建和编辑 TwinCAT 3 Scope 工程](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/182322699.html) | 同时采集命令位置、实际位置、偏差、压力与状态位，利用标尺比较时间差。 |
| [D17](#d17) | [Scope nodes：录制时间、环形缓冲与自动保存](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/6192246155.html) | 延长 YT 录制；在故障前保留环形历史；大数据记录转文件缓存。 |
| [D18](#d18) | [Scope Trigger：触发组、条件与标记](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/182291083.html) | 用真空不到位、摆杆超限或 Error 上升沿定位异常区间。 |
| [D19](#d19) | [WcState：循环过程数据是否有效](https://infosys.beckhoff.com/content/1033/b110_ethercat_optioninterface/1984417163.html) | 设备动作许可除 OP 状态外还检查 WcState，避免用无效过程数据做联锁。 |
| [D20](#d20) | [EtherCAT Online：CRC、丢帧与 Tx/Rx 错误](https://infosys.beckhoff.com/content/1033/tc3_io_intro/1446518411.html) | 区分线缆/接触问题、设备状态异常和网卡收发损失；清零前先留证据。 |
| [D21](#d21) | [Distributed Clocks Diagnosis：时钟偏差统计](https://infosys.beckhoff.com/content/1033/tc3_io_intro/1446577547.html) | 高速多轴同步不稳时，从 DC 偏差分布检查同步质量。 |
| [D22](#d22) | [Distributed Clocks Slave Diagnosis：帧时序诊断](https://infosys.beckhoff.com/content/1033/tc3_io_intro/1446579467.html) | 验证 EtherCAT 帧是否赶在从站采样/输出窗口前到达，分析同步窗口余量。 |
| [D23](#d23) | [CoE Online、PLC 访问与 Startup 列表](https://infosys.beckhoff.com/content/1033/elm3xxx/11769061515.html) | 在线参数改后重启恢复、换模块后参数丢失时，分别核对在线值和启动下载值。 |
| [D24](#d24) | [Wireshark：构建显示过滤器](https://www.wireshark.org/docs/wsug_html_chunked/ChWorkBuildDisplayFilterSection.html) | 用 IP、tcp.port、tcp.stream 精确筛选 PLC 与视觉设备通信。 |
| [D25](#d25) | [Wireshark：TCP Analysis](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvTCPAnalysis.html) | 排查视觉响应变慢时区分网络重传/窗口阻塞与应用处理延迟。 |
| [D26](#d26) | [Wireshark：Time Stamps 的来源与精度](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvTimestamps.html) | 相机通信计时报告注明抓包点与网卡；避免将 PC 时间戳直接当相机曝光时刻。 |
| [D27](#d27) | [Wireshark：Follow TCP/UDP Streams](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvFollowStreamSection.html) | 识别视觉请求/结果报文、分包与拼包，避免把任意 ACK 当作识别完成。 |
| [D28](#d28) | [Wireshark：TCP 字段参考](https://www.wireshark.org/docs/dfref/t/tcp.html) | 建立可复用过滤器和导出列，辅助统计重传、会话和有效负载。 |
| [D29](#d29) | [Wireshark：时间显示与参考点](https://www.wireshark.org/docs/wsug_html_chunked/ChWorkTimeFormatsSection.html) | 以某次视觉请求为时间参考，测量匹配的结果响应时间；避免过滤后错读相邻包差。 |
| [D30](#d30) | [Implicit checks：数组、指针和除零检查](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527298443.html) | 定位偶发异常、越界或非法指针，结合 core dump 分析具体位置。 |
| [D31](#d31) | [Scope ADS Acquisition：任务采样与采样周期](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/10380004619.html) | 采集毫秒级真空与动作顺序时对齐任务采样；核对变量端口与符号，避免误采样。 |

<a id="d01"></a>
## D01 · Real-Time：调度、任务超周期与 I/O 更新时间

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_grundlagen/6828869003.html)

介绍抢占调度、周期超时行为、隔离核和 I/O at task start 的时间关系。

- 用于：高速设备节拍不稳定时，区分任务运算超时、输出更新时间波动及跨任务延迟。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：TwinCAT 3；不同 OS/运行时功能以对应版本为准。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d02"></a>
## D02 · Real-Time Online：CPU 负载与系统延迟

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_system/5206501899.html)

Online 页面显示当前及历史实时 CPU 负载、CPU Limit 与系统延迟。

- 用于：程序运行前后对比负载和延迟，建立可复现的性能基线。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：TwinCAT 3 System 文档。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d03"></a>
## D03 · FB_ReadTaskExceedCounter：读取任务超周期计数

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_system/11267603979.html)

读取指定任务 Exceed Counter，并提供 Busy/Error/ErrorID。

- 用于：将超周期计数纳入设备诊断；验证大循环、文件处理或批量数据计算是否造成超时。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：TwinCAT >= 3.1.4024.22；Tc2_System >= 3.4.25.0。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d04"></a>
## D04 · Project tab：PLC Boot Project 自启动

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_userinterface/3434440203.html)

解释 Autostart boot project；该设置直接写入当前目标系统，并不保存在 TwinCAT 工程中。

- 用于：换 PLC、还原工程后，检查为何 TwinCAT 已 RUN 而 PLC 未自动启动。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：TwinCAT 3；目标机设置与工程配置分开核对。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d05"></a>
## D05 · PLC Settings：启动超时、Boot 更新与持久化备份

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_userinterface/3434442123.html)

覆盖 Boot 更新策略、持久化备份、指针恢复、无效符号记录及启动超时。

- 用于：断电重启异常、旧 bootdata 回读、Online Change 后重启程序回退时查此页。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：Boot 更新选项：4026 起；指针恢复：4026.11 起；启动超时：4024.66/4026.14 起，4024.35 不适用新增选项。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d06"></a>
## D06 · Remanent Variables：PERSISTENT 与 RETAIN

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2528803467.html)

对比保持变量的存储条件、复位/下载行为，以及启动时声明值、FB_Init、bootdata 的初始化顺序。

- 用于：配方、计数器和设备标定数据断电丢失或重启恢复旧值时，核对保存机制。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：RETAIN 依赖对应硬件保持区；PERSISTENT 默认需正常关闭/UPS 或显式写入。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d07"></a>
## D07 · FB_WritePersistentData：显式保存持久数据

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_utilities/35030155.html)

介绍持久数据写入 FB，MODE 可影响数据一致性和任务超周期行为。

- 用于：配方变更后受控保存，记录 Busy/ERR/ERRID；避免把周期调用等同于每周期保存。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：TwinCAT 3.1；Tc2_Utilities；模式与存储负荷需现场确认。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d08"></a>
## D08 · Command Online Change：在线修改边界

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2531444363.html)

解释 Fast Online Change、初始化差异、指针迁移风险及导致必须下载的变更。

- 用于：修改 FB、接口或隐式检查前评估是否能在线修改，避免误把保留状态当重新初始化。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：与 4026.11 指针恢复设置合读；旧版本需手工重新赋值指针。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d09"></a>
## D09 · FB_init / FB_reinit / FB_exit：生命周期与异常

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/5044757003.html)

介绍系统隐式调用的初始化/退出方法，以及这些方法发生异常时生成 core dump 的行为。

- 用于：定位激活/启动阶段崩溃，检查初始化代码、引用和指针；避免随意显式调用生命周期方法。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：异常自动 core dump 从 4024.25 起；4026 起存储目录发生变化。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d10"></a>
## D10 · Error analysis with core dump：离线崩溃定位

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/6884133515.html)

介绍 core dump 创建、读取与归档；必须保留关联工程和匹配 compileinfo 才能加载。

- 用于：现场偶发崩溃时一起归档 .core、工程和 .compileinfo，保留可离线分析的证据。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：不同 Build 存储目录/自动归档行为需按页面分项核对。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d11"></a>
## D11 · Flow Control：观察执行位置上的实际值

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527642507.html)

流程控制可显示语句实际执行位置与执行时的值；普通监视只显示周期间值。

- 用于：追踪同一扫描中变量先后赋值、条件命中、流程跳步等问题。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：启用会增加 PLC 运行时间；选择任务功能从 4026.11 起。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d12"></a>
## D12 · Use of breakpoints：条件断点和执行点

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527568011.html)

说明断点、条件/命中次数及不停止程序的执行点。

- 用于：离线/可控工况定位罕见分支；用条件执行点辅助计数。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：命中断点会停止该 PLC 工程内所有任务的代码执行，工程外代码仍可能执行。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d13"></a>
## D13 · Using Watchlists：集中监视变量

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527704459.html)

建立监视列表、添加变量与结构体，并说明在线准备写入/强制值的入口。

- 用于：为一个故障集中保存请求、许可、状态、步号、Done/Error 与联锁变量。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：TwinCAT 3 PLC；写入/强制会影响运行，观察与改值分别操作。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d14"></a>
## D14 · EventLogger Technical introduction：消息与报警模型

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_eventlogger/4278578443.html?id=2759979561564329345)

解释事件类、Event ID、Source Info、消息和有状态报警及缓存架构。

- 用于：建立模块化报警来源和首故障记录，减少只看当前报警而丢失前因的问题。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：缓存依赖安全关机；Windows CE 从 4024.25 起缓存不持久化。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d15"></a>
## D15 · EventLogger PLC Tutorial：首个事件

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_eventlogger/4279107979.html)

从 Type System 定义事件，到引入 Tc3_EventLogger 并发送 PLC 消息的教程。

- 用于：把现有模块故障码逐步接入统一事件记录，不必一次重构全机。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：PLC 版本教程；不要误用旁边 C++ API 教程。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d16"></a>
## D16 · 创建和编辑 TwinCAT 3 Scope 工程

[打开原始资料](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/182322699.html)

包含 Measurement Wizard、变量选择、YT 图、标尺差值与数据导出。

- 用于：同时采集命令位置、实际位置、偏差、压力与状态位，利用标尺比较时间差。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：基础/专业版功能按 Scope 许可核对；暂停显示不等于停止采集。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d17"></a>
## D17 · Scope nodes：录制时间、环形缓冲与自动保存

[打开原始资料](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/6192246155.html)

Record Time、Ring buffer、File Store、Auto Save 等记录级设置的直接入口。

- 用于：延长 YT 录制；在故障前保留环形历史；大数据记录转文件缓存。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：以当前安装 Scope 版本和许可为准；自动删除选项需明确设置。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d18"></a>
## D18 · Scope Trigger：触发组、条件与标记

[打开原始资料](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/182291083.html)

触发条件可逻辑组合，用于开始/停止记录或标记事件；Marker 可计算时间和数值差。

- 用于：用真空不到位、摆杆超限或 Error 上升沿定位异常区间。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：TwinCAT 3 Scope；具体动作和功能需匹配许可。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d19"></a>
## D19 · WcState：循环过程数据是否有效

[打开原始资料](https://infosys.beckhoff.com/content/1033/b110_ethercat_optioninterface/1984417163.html)

Working Counter State 指示从站是否正确参与循环数据交换。

- 用于：设备动作许可除 OP 状态外还检查 WcState，避免用无效过程数据做联锁。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：页面以 B110 接口说明；具体从站 PDO/诊断位以设备手册为准。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d20"></a>
## D20 · EtherCAT Online：CRC、丢帧与 Tx/Rx 错误

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_io_intro/1446518411.html)

说明主站/从站在线状态、各端口 CRC、Lost Frames 与网卡 Tx/Rx Errors。

- 用于：区分线缆/接触问题、设备状态异常和网卡收发损失；清零前先留证据。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：TwinCAT 3 I/O 官方参考；CRC 按端口 A/B/C/D 查看。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d21"></a>
## D21 · Distributed Clocks Diagnosis：时钟偏差统计

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_io_intro/1446577547.html)

介绍 DC 偏差分布、正负计数和主站与参考时钟的漂移比例。

- 用于：高速多轴同步不稳时，从 DC 偏差分布检查同步质量。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：诊断运行模式和 Sync Unit 条件以页面为准；统计值不等同于单轴机械误差。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d22"></a>
## D22 · Distributed Clocks Slave Diagnosis：帧时序诊断

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_io_intro/1446579467.html)

测量并导出从站 SoF/EoF、SYNC、PDI 之间的时序关系。

- 用于：验证 EtherCAT 帧是否赶在从站采样/输出窗口前到达，分析同步窗口余量。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：需要存在使用 DC 的帧和设备；可导出 DC Diagnostics XML。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d23"></a>
## D23 · CoE Online、PLC 访问与 Startup 列表

[打开原始资料](https://infosys.beckhoff.com/content/1033/elm3xxx/11769061515.html)

说明在线 CoE、Tc2_EtherCAT 与 ADS Monitor 访问，并介绍参数放入 Startup 列表。

- 用于：在线参数改后重启恢复、换模块后参数丢失时，分别核对在线值和启动下载值。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：以 ELM3xxx 为例；第三方模块参数持久化和状态转换时机必须查该厂商手册。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d24"></a>
## D24 · Wireshark：构建显示过滤器

[打开原始资料](https://www.wireshark.org/docs/wsug_html_chunked/ChWorkBuildDisplayFilterSection.html)

官方显示过滤语法，支持字段比较及逻辑组合。

- 用于：用 IP、tcp.port、tcp.stream 精确筛选 PLC 与视觉设备通信。
- 来源：Wireshark 项目官方（一手资料）；语言：English；类型：官方在线文档
- 版本与边界：显示过滤器与 Capture Filter 语法不同；字段以安装版本为准。
- 获取/许可：Wireshark User’s Guide 标明 GPL；本汇总仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d25"></a>
## D25 · Wireshark：TCP Analysis

[打开原始资料](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvTCPAnalysis.html)

说明重传、乱序、重复 ACK、窗口等 TCP 分析标记及判断基础。

- 用于：排查视觉响应变慢时区分网络重传/窗口阻塞与应用处理延迟。
- 来源：Wireshark 项目官方（一手资料）；语言：English；类型：官方在线文档
- 版本与边界：分析依赖捕获完整性；suspected 标记不能单独证明线路丢包。
- 获取/许可：Wireshark User’s Guide 标明 GPL；本汇总仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d26"></a>
## D26 · Wireshark：Time Stamps 的来源与精度

[打开原始资料](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvTimestamps.html)

说明时间戳来自捕获库/系统，显示精度不代表实际捕获精度。

- 用于：相机通信计时报告注明抓包点与网卡；避免将 PC 时间戳直接当相机曝光时刻。
- 来源：Wireshark 项目官方（一手资料）；语言：English；类型：官方在线文档
- 版本与边界：精度取决于 OS/捕获系统；需要精确计时时官方不建议 USB 网卡。
- 获取/许可：Wireshark User’s Guide 标明 GPL；本汇总仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d27"></a>
## D27 · Wireshark：Follow TCP/UDP Streams

[打开原始资料](https://www.wireshark.org/docs/wsug_html_chunked/ChAdvFollowStreamSection.html)

按会话重组协议字节流，并查看通信两端数据。

- 用于：识别视觉请求/结果报文、分包与拼包，避免把任意 ACK 当作识别完成。
- 来源：Wireshark 项目官方（一手资料）；语言：English；类型：官方在线文档
- 版本与边界：按实际应用层协议识别完成报文；TCP 包边界不代表应用消息边界。
- 获取/许可：Wireshark User’s Guide 标明 GPL；本汇总仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d28"></a>
## D28 · Wireshark：TCP 字段参考

[打开原始资料](https://www.wireshark.org/docs/dfref/t/tcp.html)

提供 tcp.stream、tcp.len、tcp.analysis.* 等字段类型和适用版本。

- 用于：建立可复用过滤器和导出列，辅助统计重传、会话和有效负载。
- 来源：Wireshark 项目官方（一手资料）；语言：English；类型：官方在线文档
- 版本与边界：字段页逐项列出支持版本；部署时以所装版本验证。
- 获取/许可：Wireshark 官方资料；本页未单独核实再分发条款，仅收录链接和原创摘要。
- 核验：opened，2026-10-17

<a id="d29"></a>
## D29 · Wireshark：时间显示与参考点

[打开原始资料](https://www.wireshark.org/docs/wsug_html_chunked/ChWorkTimeFormatsSection.html)

区别上一捕获包/上一显示包时间差，并说明 Time Reference 的用法。

- 用于：以某次视觉请求为时间参考，测量匹配的结果响应时间；避免过滤后错读相邻包差。
- 来源：Wireshark 项目官方（一手资料）；语言：English；类型：官方在线文档
- 版本与边界：Time Reference 不会永久写入捕获文件；记录分析规则以便复现。
- 获取/许可：Wireshark User’s Guide 标明 GPL；本汇总仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d30"></a>
## D30 · Implicit checks：数组、指针和除零检查

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527298443.html)

官方隐式检查入口可检查数组边界、子范围、指针及除零。

- 用于：定位偶发异常、越界或非法指针，结合 core dump 分析具体位置。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：添加/移除隐式检查可能影响 Online Change，先检查下载要求和运行负荷。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17

<a id="d31"></a>
## D31 · Scope ADS Acquisition：任务采样与采样周期

[打开原始资料](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/10380004619.html)

解释 SampleTime、UseTaskSampleTime、Symbol based、TargetPort 和本地/远端 Scope Server。

- 用于：采集毫秒级真空与动作顺序时对齐任务采样；核对变量端口与符号，避免误采样。
- 来源：Beckhoff 官方（一手厂商资料）；语言：English；类型：官方在线文档
- 版本与边界：新旧 Scope 工程界面可能不同；TimeOffset 只是人为校正，应有测量依据。
- 获取/许可：© Beckhoff Automation；未核实全文再分发许可，仅收录链接和原创中文摘要。
- 核验：opened，2026-10-17
