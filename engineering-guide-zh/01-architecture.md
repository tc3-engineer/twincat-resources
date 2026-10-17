# 架构与规范

核验日期：2026-10-17 · 27 项。返回[总目录](README.md)。

| 编号 | 资源 | 主要用途 |
|---|---|---|
| [A01](#a01) | [PLC programming conventions](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12049233675.html) | 建立团队代码评审和基础库规范；重点读输出单写者、错误处理、枚举、多任务部分。 |
| [A02](#a02) | [Object-oriented programming](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527303819.html) | 确定模块边界与接口；避免继承层级过深，检查接口空引用。 |
| [A03](#a03) | [OOP basic sample](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/7647320331.html) | 在独立工程练习接口替换与 FB 封装。 |
| [A04](#a04) | [Object-oriented program for controlling a sorting plant](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/100978955.html) | 用于设计气缸、真空、轴设备层及工位层的分层边界。 |
| [A05](#a05) | [Object Interface](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/4256428299.html) | 给抓手、气缸、运动设备定义稳定契约，替换具体硬件实现。 |
| [A06](#a06) | [ABSTRACT concept](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/6413748235.html) | 复用设备模块公共行为，同时强制子类实现关键操作。 |
| [A07](#a07) | [Pointers, references, interfaces](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12050043147.html) | 排查 RF/REFERENCE 失效、空接口调用、方法局部变量地址逃逸。 |
| [A08](#a08) | [Implementation of function blocks](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12081376523.html) | 规范 CSV记录、通讯、凸轮生成等耗时 FB 的启动、忙、结果与错误边界。 |
| [A09](#a09) | [Multiple tasks](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12050040971.html) | 审查运动快任务、通讯慢任务、数据记录任务的共享数据和写入者。 |
| [A10](#a10) | [Performing an Online Change](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2528041355.html) | 判断局部修改是否触发初始化；分析参数变更为何未生效及指针失效。 |
| [A11](#a11) | [Allocated variables](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12081664011.html) | 梳理自动/手动/复位同时写电磁阀或真空输出导致的扫描覆盖。 |
| [A12](#a12) | [Packaging Machine State — Tc3_PackML_V2](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1335919755.html) | 设计整机 PackML 状态、设备模块过程和完成反馈之间的关系。 |
| [A13](#a13) | [PML_StateMachine](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1335962123.html) | 统一整机与工位状态汇总，避免把子动作完成误当整机完成。 |
| [A14](#a14) | [PML_UnitModeManager](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1336429067.html) | 设计自动、手动、维护、空叠等模式请求、许可、完成确认链。 |
| [A15](#a15) | [PLCopen Software Construction Guidelines](https://www.plcopen.org/guidelines/software-construction-guidelines/) | 建立跨品牌也适用的 PLC 软件工程学习与评审目录。 |
| [A16](#a16) | [PLCopen Coding Guidelines v1.0](https://www.plcopen.org/download_file/force/ff60e817-eee5-442d-b718-a357a7279c7e/342/) | 为现有项目做低风险代码审查，优先找重复写输出、未检查错误和跨任务共享。 |
| [A17](#a17) | [PLCopen Guidelines for usage of OOP v1.0](https://www.plcopen.org/download_file/force/14f8df00-91d6-45d6-a161-76f9b5895210/342/) | 给老工程局部增加接口和诊断，而非先进行整机重写。 |
| [A18](#a18) | [Creating PLCopen compliant Function Block libraries](https://www.plcopen.org/download_file/view/7ea712b1-1f89-43fc-870c-6006e415956f/) | 设计文件、通讯和计算 FB，确保完成、取消、超时和复位语义一致。 |
| [A19](#a19) | [PLCopen Structuring with SFC: do’s and don’ts v1.0](https://www.plcopen.org/download_file/force/5f66721e-9586-43d0-9f7c-79faa00e9ae4/342/) | 排查并行流程重复进入、转换条件冲突、状态退出动作遗漏。 |
| [A20](#a20) | [PackML 官方入口与实施指南](https://www.omac.org/packml) | 用标准源头校正 Held/Suspended/Stopped 与模式定义。 |
| [A21](#a21) | [IEC 61131-3: The State Pattern](https://stefanhenneken.net/2018/11/17/iec-61131-3-the-state-pattern/) | 为大型设备状态机选择适当拆分方式；小流程可保留 CASE。 |
| [A22](#a22) | [State Pattern Sample03](https://github.com/StefanHenneken/Blog-2018-06-IEC61131-StatePattern-Sample03) | 单独导入学习接口与状态 FB 的协作，保留原始许可后可纳入示例目录。 |
| [A23](#a23) | [IEC 61131-3: The Observer Pattern](https://stefanhenneken.net/2018/05/27/iec-61131-3-the-observer-pattern/) | 报警、状态变化通知等适用场景；运动关键路径要明确调用顺序和执行耗时。 |
| [A24](#a24) | [IEC 61131-3: The Command Pattern](https://stefanhenneken.net/2016/12/07/iec-61131-3-the-command-pattern/) | 组织手动操作、设备命令分派与诊断记录。 |
| [A25](#a25) | [IEC 61131-3: The Decorator Pattern](https://stefanhenneken.net/2019/02/16/iec-61131-3-the-decorator-pattern/) | 在通用设备外围增加统计或日志能力，评估其复杂度是否值得。 |
| [A26](#a26) | [TwinCAT 3 course — AllTwinCAT](https://alltwincat.com/twincat-3-tutorial/) | 有经验工程师优先学习 6a/6b、9、11、13～17 部分。 |
| [A27](#a27) | [tc3-packml-sample-01](https://github.com/shawnbgit/tc3-packml-sample-01) | 研究 PackML 整机与工位层级状态传播；作为阅读样本而非可直接投产框架。 |

<a id="a01"></a>
## A01 · PLC programming conventions

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12049233675.html)

官方统一编程风格、命名与代码规则，并提供静态分析配置下载入口。

- 用于：建立团队代码评审和基础库规范；重点读输出单写者、错误处理、枚举、多任务部分。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：文档入口
- 版本与边界：规则区分强制项与建议项；Static Analysis Light 自 Build 4018 提供。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a02"></a>
## A02 · Object-oriented programming

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527303819.html)

覆盖 FB、方法、属性、接口、继承以及 OOP 粒度取舍。

- 用于：确定模块边界与接口；避免继承层级过深，检查接口空引用。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：官方指南
- 版本与边界：不同 OOP 特性存在 Build 门槛；不能把当前在线文档全部套入旧编译器。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a03"></a>
## A03 · OOP basic sample

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/7647320331.html)

演示方法、属性、继承及接口实现；页面有 TC3_PlcSample_OOPBasicSample.zip。

- 用于：在独立工程练习接口替换与 FB 封装。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：官方示例工程入口
- 版本与边界：已核验入口；ZIP 未由网页工具成功展开，导入前核对项目版本。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a04"></a>
## A04 · Object-oriented program for controlling a sorting plant

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/100978955.html)

以气缸接口、派生模块和子系统构成分拣机，提供 PLC 与模拟 PLC 工程。

- 用于：用于设计气缸、真空、轴设备层及工位层的分层边界。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：官方完整示例
- 版本与边界：示例为 TC3.1；官方明确其概念不可不加判断地推广到所有应用；ZIP 未展开。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a05"></a>
## A05 · Object Interface

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/4256428299.html)

解释 INTERFACE 原型、实现要求与通过接口访问不同 FB。

- 用于：给抓手、气缸、运动设备定义稳定契约，替换具体硬件实现。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：API语言文档
- 版本与边界：接口变量与对象生命周期、在线修改行为需结合目标 Build 检查。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a06"></a>
## A06 · ABSTRACT concept

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/6413748235.html)

说明抽象 FB、方法、属性及派生类实现规则。

- 用于：复用设备模块公共行为，同时强制子类实现关键操作。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：语言文档
- 版本与边界：明确从 TwinCAT 3.1 Build 4024 起支持。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a07"></a>
## A07 · Pointers, references, interfaces

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12050043147.html)

覆盖临时对象引用、在线修改地址变化、空引用检查和短路求值。

- 用于：排查 RF/REFERENCE 失效、空接口调用、方法局部变量地址逃逸。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：规范与正反例
- 版本与边界：静态对象引用需按官方规则重新绑定；动态对象生命周期另行处理。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a08"></a>
## A08 · Implementation of function blocks

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12081376523.html)

区分一次性 bExecute 与连续 bEnable 模式，并定义 Busy、Valid、Error 行为。

- 用于：规范 CSV记录、通讯、凸轮生成等耗时 FB 的启动、忙、结果与错误边界。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：接口规范
- 版本与边界：该页示例以异步 ADS 为背景；不要混淆其完成语义和 PLCopen MC 的 Done 语义。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a09"></a>
## A09 · Multiple tasks

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12050040971.html)

说明共享数据及同一 FB 跨任务访问的风险，建议通过参数传递依赖。

- 用于：审查运动快任务、通讯慢任务、数据记录任务的共享数据和写入者。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：规范与正反例
- 版本与边界：同一 FB 多任务访问默认不允许，除非其文档明确为该用途设计。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a10"></a>
## A10 · Performing an Online Change

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2528041355.html)

解释在线修改保留运行状态、快速在线修改及哪些改动会要求下载。

- 用于：判断局部修改是否触发初始化；分析参数变更为何未生效及指针失效。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：操作与运行语义
- 版本与边界：继承基类、接口列表、任务配置等改动可能不支持在线修改；以实际工程提示为准。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a11"></a>
## A11 · Allocated variables

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12081664011.html)

介绍自动地址分配、避免输出多处写入和地址重叠。

- 用于：梳理自动/手动/复位同时写电磁阀或真空输出导致的扫描覆盖。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：规范与正反例
- 版本与边界：SA0004 输出多处写入检查包含于免费 Static Analysis Light。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a12"></a>
## A12 · Packaging Machine State — Tc3_PackML_V2

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1335919755.html)

说明标准状态机与应用专属状态动作及转换逻辑的职责边界。

- 用于：设计整机 PackML 状态、设备模块过程和完成反馈之间的关系。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：库总体说明
- 版本与边界：页面列 Build 4018+、PC i386、Tc3_PackML_V2；旧库说明不等于对当前 x64 兼容性验证。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a13"></a>
## A13 · PML_StateMachine

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1335962123.html)

提供 Production/Maintenance/Manual 状态模型与下级单元状态引用。

- 用于：统一整机与工位状态汇总，避免把子动作完成误当整机完成。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：FB接口文档
- 版本与边界：Tc3_PackML_V2，文档列 Build 4018+、i386；应锁定现场库版本。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a14"></a>
## A14 · PML_UnitModeManager

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1336429067.html)

根据当前状态管理 UnitMode 切换，避免不适当状态下直接换模式。

- 用于：设计自动、手动、维护、空叠等模式请求、许可、完成确认链。
- 来源：官方（Beckhoff InfoSys）；语言：en；类型：FB接口文档
- 版本与边界：标准三种模式已有边界；自定义空叠模式与工艺重算仍需应用自行设计。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a15"></a>
## A15 · PLCopen Software Construction Guidelines

[打开原始资料](https://www.plcopen.org/guidelines/software-construction-guidelines/)

集中连接 Coding、FB 库、SFC、OOP、运动 OOP 与软件质量指标六类指南。

- 用于：建立跨品牌也适用的 PLC 软件工程学习与评审目录。
- 来源：行业组织官方（PLCopen）；语言：en；类型：官方文档总入口
- 版本与边界：各文档发布时间不同，指南不代表具体 TwinCAT API 实现。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a16"></a>
## A16 · PLCopen Coding Guidelines v1.0

[打开原始资料](https://www.plcopen.org/download_file/force/ff60e817-eee5-442d-b718-a357a7279c7e/342/)

完整命名、注释、复杂度、任务同步、单写者与 FB 使用规范。

- 用于：为现有项目做低风险代码审查，优先找重复写输出、未检查错误和跨任务共享。
- 来源：行业组织官方（PLCopen）；语言：en；类型：PDF（127页）
- 版本与边界：2016-04-20 官方版 1.0；语法细节结合 TwinCAT 当前编译器。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a17"></a>
## A17 · PLCopen Guidelines for usage of OOP v1.0

[打开原始资料](https://www.plcopen.org/download_file/force/14f8df00-91d6-45d6-a161-76f9b5895210/342/)

以锅炉例子说明模块与命令对象、渐进式 OOP 改造、统一行为和错误管理。

- 用于：给老工程局部增加接口和诊断，而非先进行整机重写。
- 来源：行业组织官方（PLCopen）；语言：en；类型：PDF（27页）
- 版本与边界：2021-11-18 官方版；附属示例是 CODESYS 工程，需迁移而非直接假定 TwinCAT 可编译。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a18"></a>
## A18 · Creating PLCopen compliant Function Block libraries

[打开原始资料](https://www.plcopen.org/download_file/view/7ea712b1-1f89-43fc-870c-6006e415956f/)

概述 Execute/Enable、Done/Valid、Abort、TimeOut 与分周期 TimeLimit。

- 用于：设计文件、通讯和计算 FB，确保完成、取消、超时和复位语义一致。
- 来源：行业组织官方（PLCopen）；语言：en；类型：PDF概述（4页）
- 版本与边界：本条是4页概述；完整 v1.0 从官方 Downloads 获取，网页解析因大于10MB失败。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a19"></a>
## A19 · PLCopen Structuring with SFC: do’s and don’ts v1.0

[打开原始资料](https://www.plcopen.org/download_file/force/5f66721e-9586-43d0-9f7c-79faa00e9ae4/342/)

覆盖步与转换、并行合流、动作独立性、Final Scan，以及 PackML 到 SFC 的映射。

- 用于：排查并行流程重复进入、转换条件冲突、状态退出动作遗漏。
- 来源：行业组织官方（PLCopen）；语言：en；类型：PDF（59页）
- 版本与边界：2018-07-03 官方版；具体 SFC 执行需结合 TwinCAT 文档。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a20"></a>
## A20 · PackML 官方入口与实施指南

[打开原始资料](https://www.omac.org/packml)

链接 ISA 标准及 2022/2015 实施资料，明确 PackML 的状态与数据接口定位。

- 用于：用标准源头校正 Held/Suspended/Stopped 与模式定义。
- 来源：行业组织官方（OMAC）；语言：en；类型：标准与指南入口
- 版本与边界：2022 Implementation Guide Part 1 页面标 v2.03、基于 TR88.00.02-2022；全文需会员或购买。
- 获取/许可：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- 核验：opened，2026-10-17

<a id="a21"></a>
## A21 · IEC 61131-3: The State Pattern

[打开原始资料](https://stefanhenneken.net/2018/11/17/iec-61131-3-the-state-pattern/)

比较 CASE、方法拆分和 State Pattern 三种实现，讨论规模与维护取舍。

- 用于：为大型设备状态机选择适当拆分方式；小流程可保留 CASE。
- 来源：作者一手（Stefan Henneken；社区）；语言：en；类型：教程与示例链接
- 版本与边界：示例标 TwinCAT 3.1.4022；文章更新记录不等同于已对4026重新验证。
- 获取/许可：文章无已核验全文转载许可；示例仓库另有 BSD-2-Clause。
- 核验：opened，2026-10-17

<a id="a22"></a>
## A22 · State Pattern Sample03

[打开原始资料](https://github.com/StefanHenneken/Blog-2018-06-IEC61131-StatePattern-Sample03)

State Pattern 原作者第三种实现的完整 TwinCAT 示例工程。

- 用于：单独导入学习接口与状态 FB 的协作，保留原始许可后可纳入示例目录。
- 来源：作者一手（Stefan Henneken；社区）；语言：en；类型：源码仓库
- 版本与边界：文章标 3.1.4022；未在本环境执行 TwinCAT 编译或现场运行。
- 获取/许可：BSD-2-Clause；已打开仓库 LICENSE 核验，复制须保留版权、条件与免责声明。
- 核验：opened，2026-10-17

<a id="a23"></a>
## A23 · IEC 61131-3: The Observer Pattern

[打开原始资料](https://stefanhenneken.net/2018/05/27/iec-61131-3-the-observer-pattern/)

通过接口和订阅关系减少一对多状态通知的硬连接。

- 用于：报警、状态变化通知等适用场景；运动关键路径要明确调用顺序和执行耗时。
- 来源：作者一手（Stefan Henneken；社区）；语言：en；类型：教程
- 版本与边界：示例标 TwinCAT 3.1.4022；不应直接解释成跨任务线程安全事件总线。
- 获取/许可：未核验文章转载许可；链接及原创摘要，代码按各示例仓库 LICENSE 另审。
- 核验：opened，2026-10-17

<a id="a24"></a>
## A24 · IEC 61131-3: The Command Pattern

[打开原始资料](https://stefanhenneken.net/2016/12/07/iec-61131-3-the-command-pattern/)

介绍命令调用方与接收设备解耦、组合命令及命令记录的思路。

- 用于：组织手动操作、设备命令分派与诊断记录。
- 来源：作者一手（Stefan Henneken；社区）；语言：en；类型：教程
- 版本与边界：示例标 TwinCAT 3.1.4020；Undo 示意不能直接当作实际机械动作安全回退。
- 获取/许可：未核验文章转载许可；链接及原创摘要，代码按各示例仓库 LICENSE 另审。
- 核验：opened，2026-10-17

<a id="a25"></a>
## A25 · IEC 61131-3: The Decorator Pattern

[打开原始资料](https://stefanhenneken.net/2019/02/16/iec-61131-3-the-decorator-pattern/)

通过组合叠加行为，展示替代不断增加继承层级的方式。

- 用于：在通用设备外围增加统计或日志能力，评估其复杂度是否值得。
- 来源：作者一手（Stefan Henneken；社区）；语言：en；类型：教程
- 版本与边界：示例标 TwinCAT 3.1.4022；应评估额外间接调用和对象生命周期。
- 获取/许可：未核验文章转载许可；链接及原创摘要，代码按各示例仓库 LICENSE 另审。
- 核验：opened，2026-10-17

<a id="a26"></a>
## A26 · TwinCAT 3 course — AllTwinCAT

[打开原始资料](https://alltwincat.com/twincat-3-tutorial/)

18部分课程覆盖 FB/接口、任务、文件日志、库、Git、ADS、版本管理与测试。

- 用于：有经验工程师优先学习 6a/6b、9、11、13～17 部分。
- 来源：作者一手（Jakob Sagatowski；社区）；语言：en；类型：视频课程索引
- 版本与边界：课程跨多年发布；安装/系统要求及工具界面以当前 Beckhoff 文档为准。
- 获取/许可：免费观看不代表允许视频或全文再分发；收录作者原链接。
- 核验：opened，2026-10-17

<a id="a27"></a>
## A27 · tc3-packml-sample-01

[打开原始资料](https://github.com/shawnbgit/tc3-packml-sample-01)

示例区分生产线主控、Unit 与 SubUnit，并带简单可视化。

- 用于：研究 PackML 整机与工位层级状态传播；作为阅读样本而非可直接投产框架。
- 来源：作者一手（shawnbgit；社区）；语言：en；类型：源码仓库
- 版本与边界：作者标明 TwinCAT Build 4024.32；本环境未编译验证。
- 获取/许可：仓库根目录未发现 LICENSE；仅收录链接，不默认允许复制重发布。
- 核验：opened，2026-10-17
