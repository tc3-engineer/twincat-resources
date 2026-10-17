# 运动控制与凸轮

核验日期：2026-10-17 · 25 项。返回[总目录](README.md)。

| 编号 | 资源 | 主要用途 |
|---|---|---|
| [M01](#m01) | [General rules for MC function blocks｜PLCopen 调用通则](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70043531.html) | 查动作不触发、忙信号不退出、假完成、同轴多命令抢占；设计可审核的轴命令封装。 |
| [M02](#m02) | [State diagram｜PLCopen 单轴状态图](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70041995.html) | 梳理总流程、暂停恢复、复位再启动以及主从轴耦合时机。 |
| [M03](#m03) | [MC_ReadStatus｜每周期轴状态刷新](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70066187.html) | 避免流程读取过期的 StandStill、SynchronizedMotion 或 ErrorStop 状态。 |
| [M04](#m04) | [MC_Stop｜停止与轴锁定释放](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70108555.html) | 解决停止后无法再启动、复位依赖混乱，以及普通暂停与受控停止的接口设计。 |
| [M05](#m05) | [MC_BufferMode｜命令缓冲与速度衔接](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70147595.html) | 排查节拍轴中位到零位掉速、运动接续和同一实例重触发失败。 |
| [M06](#m06) | [MC_MoveModulo｜模定位](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70099339.html) | 循环节拍轴、单向转盘和连续旋转轴定向停车。 |
| [M07](#m07) | [Notes on modulo positioning｜模定位陷阱](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70100875.html) | 排查 0° 与 360° 混用、复位后意外整圈、从实际位置计算新目标造成不稳定。 |
| [M08](#m08) | [MC_GearIn｜静止电子齿轮耦合](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70123403.html) | 排查 Master/slave 正在处理任务时耦合失败，确定耦合前状态条件。 |
| [M09](#m09) | [TF5055 PLC Library Overview｜飞锯与飞行同步](https://infosys.beckhoff.com/content/1033/tf5055_tc3_nc_flying_saw/6982976651.html) | 主轴不停机时同步从轴，区分仅速度同步与指定主从位置的同步要求。 |
| [M10](#m10) | [TF5050 Overview of the PLC library｜电子凸轮总索引](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/6961172235.html) | 为凸轮管理器建立功能清单，按具体需求查 FB 而非从旧项目盲目复制。 |
| [M11](#m11) | [MC_CamIn｜凸轮耦合与切表](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1002438027.html) | 排查切模式后凸轮不生效、排队表与当前表混淆、耦合未完成就进入下一步。 |
| [M12](#m12) | [MC_CaminAppendix｜凸轮耦合起点计算](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1002498443.html) | 解决从轴起点不一致、缓存轴闭合补偿与真空辊单向累计位移的关系。 |
| [M13](#m13) | [MC_CamActivationMode｜改表生效时机](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003600395.html) | 现场示教点更新后在指定相位/下一周期切表，避免配方参数和旧表混用。 |
| [M14](#m14) | [MC_CamScalingMode｜Autooffset 的能力边界](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003655819.html) | 评估相位不变但点位/行程变化的凸轮重算和切表策略。 |
| [M15](#m15) | [MC_CamTableSelect｜从 PLC 数组创建凸轮表](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1002328715.html) | 搭建生成—加载—校验—耦合顺序，排查密集点表的数据布局、数组容量与行数不一致。 |
| [M16](#m16) | [MC_ReadCamTableSlaveDynamics｜读取凸轮原始动态量](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003209867.html) | 耦合前起点校验、表生成后的关键点核查和动态能力评估入口。 |
| [M17](#m17) | [MC_SetCamOnlineChangeMode｜在线写点模式](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003112843.html) | 设计在线示教点更新事务，分清改数据、换表与缩放的控制入口。 |
| [M18](#m18) | [Table Errors｜NC 凸轮表错误码](https://infosys.beckhoff.com/content/1033/tc3ncerrcode/513147659.html) | 4A13 行索引越界、4A06 非单调、加载表失败等故障的第一查证入口。 |
| [M19](#m19) | [Overview of NC Errors｜NC 错误分类总表](https://infosys.beckhoff.com/content/1033/tc3ncerrcode/1521556875.html) | 用 ErrorID 确认故障层级，避免把所有轴错误都归为伺服增益或 PLC 扫描问题。 |
| [M20](#m20) | [NC PTP Monitoring｜到位与跟随误差监视](https://infosys.beckhoff.com/content/1033/tf50x0_tc3_nc_ptp/3260297099.html) | 查 0x4550 跟随误差、到位时间过长、小位移不完成、机械阻塞，以及 Done 与物理到位的差别。 |
| [M21](#m21) | [NC encoder parameters｜单位、缩放和编码器掩码](https://infosys.beckhoff.com/content/1033/tc3_ads_intro/713102219.html) | 审核单向连续转动的计数回绕配置，核对 mm、度、增量间换算和位置采样延迟。 |
| [M22](#m22) | [AX5000 First steps｜驱动调试、Startup 与单位换算](https://infosys.beckhoff.com/content/1033/ax5000_usermanual/13129565195.html) | 排查参数断电失效、轴缩放错误、转速与线速度换算和模模式溢出设置。 |
| [M23](#m23) | [AX5000 Tuning Guide｜速度环调参方法](https://infosys.beckhoff.com/content/1033/ax5000_tuning_guide/3423095179.html) | 建立先测量再调参的方法，理解空载默认参数与带负载现场表现差异。 |
| [M24](#m24) | [TE132x TwinCAT 3 Bode Plot｜机械共振与频响](https://infosys.beckhoff.com/content/1033/te132x_tc3_bodeplot/748734859.html) | 区分机械共振、控制增益过高与滤波问题，辅助高速抓手和往复轴调试。 |
| [M25](#m25) | [TE5960 Autotuning｜自动整定支持范围](https://infosys.beckhoff.com/content/1033/te5960_tc3_autotuning/16664453387.html) | 判断现场驱动是否可用官方自动整定，保存基线并比较整定后的频响。 |

<a id="m01"></a>
## M01 · General rules for MC function blocks｜PLCopen 调用通则

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70043531.html)

讲清 Execute 边沿、Busy 周期调用、输入参数采样、Done/CommandAborted/Error 以及轴错误、驱动错误和通信错误的区别；给出速度、加速度、Jerk 的工程单位。

- 用于：查动作不触发、忙信号不退出、假完成、同轴多命令抢占；设计可审核的轴命令封装。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：对应 Tc2_MC2/经典 NC；不能把通则理解成每个 FB 都实现 BufferMode，仍需核对该 FB 页。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m02"></a>
## M02 · State diagram｜PLCopen 单轴状态图

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70041995.html)

解释单轴 Disabled、Standstill、ErrorStop、Stopping 和同步运动等状态与命令的关系，区分轴状态与功能块执行错误。

- 用于：梳理总流程、暂停恢复、复位再启动以及主从轴耦合时机。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：经典 NC/Tc2_MC2。主轴可处于 ContinuousMotion、从轴处于 SynchronizedMotion，不能假设两者状态相同。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m03"></a>
## M03 · MC_ReadStatus｜每周期轴状态刷新

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70066187.html)

轴状态只需在 PLC 周期开始更新一次，后续通过 Axis.Status 读取；AXIS_REF 已包含 ReadStatus 实例。

- 用于：避免流程读取过期的 StandStill、SynchronizedMotion 或 ErrorStop 状态。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：文档要求 TwinCAT v3.0.0/Tc2_MC2；在线读取状态的顺序必须与项目任务和调用顺序一起确认。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m04"></a>
## M04 · MC_Stop｜停止与轴锁定释放

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70108555.html)

MC_Stop 停止后仍锁轴，Done 可以与 Busy/Active 同时为真；Execute 下降后还需继续调用直到 Busy 释放。

- 用于：解决停止后无法再启动、复位依赖混乱，以及普通暂停与受控停止的接口设计。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：经典 NC/Tc2_MC2；普通流程停机可比较 MC_Halt。此 FB 不能被等同于硬件安全功能。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m05"></a>
## M05 · MC_BufferMode｜命令缓冲与速度衔接

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70147595.html)

对比 Aborting、Buffered 和四种 Blending，用不同速度的图示解释连接点行为及指令下发时机。

- 用于：排查节拍轴中位到零位掉速、运动接续和同一实例重触发失败。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：需要第二个 FB 实例；文中理想混合曲线要求后续命令在前一运动减速前及时发出。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m06"></a>
## M06 · MC_MoveModulo｜模定位

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70099339.html)

解释停止与运动中启动的差别、方向限制、多圈目标、复位后的起点变化及 Done 依赖的到位监视。

- 用于：循环节拍轴、单向转盘和连续旋转轴定向停车。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：经典 NC/Tc2_MC2。运动中不能通过此 FB 反向；轴最大动态参数通常不自动限制普通 Move 命令。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m07"></a>
## M07 · Notes on modulo positioning｜模定位陷阱

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70100875.html)

详细解释绝对坐标与模坐标、模容差窗、整圈目标和复位后多转一圈；给出设定位置参与计算的理由。

- 用于：排查 0° 与 360° 混用、复位后意外整圈、从实际位置计算新目标造成不稳定。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：模位置仅为绝对位置的附加表达；不能据此断言底层编码器计数和浮点精度绝无边界。容差窗可能允许小反向修正。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m08"></a>
## M08 · MC_GearIn｜静止电子齿轮耦合

[打开原始资料](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70123403.html)

固定分子/分母齿轮比；解释静止耦合、InGear、异常抢占和脱开后的速度行为。

- 用于：排查 Master/slave 正在处理任务时耦合失败，确定耦合前状态条件。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：Tc2_MC2 的本 FB 不用于运动主轴的飞行同步，Acceleration/Deceleration/Jerk/BufferMode 在该页标记未实现；运动中脱开不自动停车。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m09"></a>
## M09 · TF5055 PLC Library Overview｜飞锯与飞行同步

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5055_tc3_nc_flying_saw/6982976651.html)

官方入口覆盖 MC_GearInVelo、MC_GearInPos 及同步阶段特征量读取。

- 用于：主轴不停机时同步从轴，区分仅速度同步与指定主从位置的同步要求。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：TF5055 产品/库范围；不要把经典 MC_GearIn 与这些 FB 的能力混为一谈，具体接口、授权和运行版本按部署确认。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m10"></a>
## M10 · TF5050 Overview of the PLC library｜电子凸轮总索引

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/6961172235.html)

集中索引加载、耦合、缩放、在线改点、多表叠加和状态读取，并明确库版本依赖。

- 用于：为凸轮管理器建立功能清单，按具体需求查 FB 而非从旧项目盲目复制。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：Tc2_MC2_Camming 从 3.4.0 起要求运行时至少 TwinCAT 3.1.4024.55；4024.35 现场不可直接假设兼容新版库。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m11"></a>
## M11 · MC_CamIn｜凸轮耦合与切表

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1002438027.html)

解释主从偏移和缩放、StartMode、ActivationMode、切表排队状态及 InSync 含义。

- 用于：排查切模式后凸轮不生效、排队表与当前表混淆、耦合未完成就进入下一步。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：TF5050/Tc2_MC2_Camming；该页 BufferMode 标明未实现，切表时机通过 Options.ActivationMode 指定。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m12"></a>
## M12 · MC_CaminAppendix｜凸轮耦合起点计算

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1002498443.html)

解释耦合前从轴必须处于凸轮对应位置，给出主从缩放/偏移换算，并讨论带净升程周期表的脱开重耦合。

- 用于：解决从轴起点不一致、缓存轴闭合补偿与真空辊单向累计位移的关系。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：示例以设定位置计算，非实际位置；普通 CamIn 不会自动平滑追入凸轮，带升程重耦合需考虑累计偏移。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m13"></a>
## M13 · MC_CamActivationMode｜改表生效时机

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003600395.html)

分别列出缩放、写点修改、首次耦合和切表可用的生效模式及坐标解释。

- 用于：现场示教点更新后在指定相位/下一周期切表，避免配方参数和旧表混用。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：按操作类别核对模式支持。ATMASTERCAMPOS 指未缩放表坐标；部分相对主轴模式有组合限制，NEXTCYCLEONCE 标注未实现。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m14"></a>
## M14 · MC_CamScalingMode｜Autooffset 的能力边界

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003655819.html)

解释手工偏移、自动偏移以及主从 Autooffset 的计算顺序与限制。

- 用于：评估相位不变但点位/行程变化的凸轮重算和切表策略。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：Autooffset 处理位置跳变，不能保证速度连续；文档建议在从轴速度为零阶段缩放。Master Autooffset 有首次耦合及相对耦合限制。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m15"></a>
## M15 · MC_CamTableSelect｜从 PLC 数组创建凸轮表

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1002328715.html)

创建并填充 NC 凸轮表，说明 Periodic、CamTableID、MC_CAM_REF 与 Done/Busy/Error。

- 用于：搭建生成—加载—校验—耦合顺序，排查密集点表的数据布局、数组容量与行数不一致。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：此接口用于 PLC 提供数据；Cam Editor 已创建表一般不需要重复调用。数组布局和指针类型须核对所安装库声明。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m16"></a>
## M16 · MC_ReadCamTableSlaveDynamics｜读取凸轮原始动态量

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003209867.html)

读取指定主轴表位置的从轴位置、速度和加速度，说明不同表类型能提供的信息差异。

- 用于：耦合前起点校验、表生成后的关键点核查和动态能力评估入口。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：读取原始表数据，不自动带入缩放；等距表加速度返回零，非等距表速度与加速度返回零，不能把这些零值当作真实动态验证。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m17"></a>
## M17 · MC_SetCamOnlineChangeMode｜在线写点模式

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003112843.html)

指定后续写入 Motion Function 点数据的生效时机，设置会影响后续写操作。

- 用于：设计在线示教点更新事务，分清改数据、换表与缩放的控制入口。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：本 FB 仅设置模式，不会自己修改或切换凸轮；SynchronousAccess 只应在确有实时需求且评估过任务负荷时考虑。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m18"></a>
## M18 · Table Errors｜NC 凸轮表错误码

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3ncerrcode/513147659.html)

提供表 ID、行列数、单调性、周期、初始化、索引和表占用的错误码分类。

- 用于：4A13 行索引越界、4A06 非单调、加载表失败等故障的第一查证入口。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：部分数值范围和旧表类型说明带有历史实现背景，必须结合当前库和 NC 版本；勿据旧表 ID 范围直接断定新版本 ID 非法。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m19"></a>
## M19 · Overview of NC Errors｜NC 错误分类总表

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3ncerrcode/1521556875.html)

按组、轴、编码器、控制器、驱动、凸轮表、NC-PLC 与扩展错误区间定位文档。

- 用于：用 ErrorID 确认故障层级，避免把所有轴错误都归为伺服增益或 PLC 扫描问题。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：优先保存十六进制原始错误码；经典 NC 与扩展 MC3 错误区间均有入口，需区分所用内核。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m20"></a>
## M20 · NC PTP Monitoring｜到位与跟随误差监视

[打开原始资料](https://infosys.beckhoff.com/content/1033/tf50x0_tc3_nc_ptp/3260297099.html)

区分 Position Lag、Position Range、Target Position、In-Target Alarm 和 Motion Monitoring。

- 用于：查 0x4550 跟随误差、到位时间过长、小位移不完成、机械阻塞，以及 Done 与物理到位的差别。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：监视窗口必须结合单位、编码器分辨率、NC 周期和真实机械响应设置；不能仅为消警把误差窗口无限放大。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m21"></a>
## M21 · NC encoder parameters｜单位、缩放和编码器掩码

[打开原始资料](https://infosys.beckhoff.com/content/1033/tc3_ads_intro/713102219.html)

查编码器缩放分子分母、模周期、掩码、计数方向、滤波和死时间补偿的参数定义与单位。

- 用于：审核单向连续转动的计数回绕配置，核对 mm、度、增量间换算和位置采样延迟。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：这是 ADS 参数参考，不是通用在线改参脚本；许多参数轴使能时禁止写入，字段/能力以具体运行时为准。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m22"></a>
## M22 · AX5000 First steps｜驱动调试、Startup 与单位换算

[打开原始资料](https://infosys.beckhoff.com/content/1033/ax5000_usermanual/13129565195.html)

覆盖 AX5000 扫描、NC 链接、Drive Manager、Startup 参数及工程单位/参考速度换算。

- 用于：排查参数断电失效、轴缩放错误、转速与线速度换算和模模式溢出设置。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：对应 AX5000/SoE，不能套用其 IDN 到高创、汇川等 CoE/DS402 设备；文中编码器分辨率是示例值。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m23"></a>
## M23 · AX5000 Tuning Guide｜速度环调参方法

[打开原始资料](https://infosys.beckhoff.com/content/1033/ax5000_tuning_guide/3423095179.html)

以 Kp、Tn 和稳定边界解释速度环响应与噪声权衡；关联章节提供 Scope 速度/扭矩对比。

- 用于：建立先测量再调参的方法，理解空载默认参数与带负载现场表现差异。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：旧版 AX5000 Guide 1.0；不是所有驱动的通用自动整定流程。文档明确持续受力的垂直轴不能照搬去积分测试方法。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m24"></a>
## M24 · TE132x TwinCAT 3 Bode Plot｜机械共振与频响

[打开原始资料](https://infosys.beckhoff.com/content/1033/te132x_tc3_bodeplot/748734859.html)

通过增益、相位、带宽和稳定裕度分析机械共振，并在应用前模拟滤波器效果。

- 用于：区分机械共振、控制增益过高与滤波问题，辅助高速抓手和往复轴调试。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：官方概述以 AX5000/AX8000 为适用驱动。4026 需单独安装 TE1320.BodePlotBase.XAE；频响记录会驱动轴实际运动。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17

<a id="m25"></a>
## M25 · TE5960 Autotuning｜自动整定支持范围

[打开原始资料](https://infosys.beckhoff.com/content/1033/te5960_tc3_autotuning/16664453387.html)

介绍频响驱动的参数和滤波器整定、结果对比以及驱动/固件支持表。

- 用于：判断现场驱动是否可用官方自动整定，保存基线并比较整定后的频响。
- 来源：Beckhoff 官方 InfoSys（一级资料）；语言：英语；类型：官方在线技术文档
- 版本与边界：支持取决于驱动和固件；AX5000 表中从 v2.15 起，AX8000 从 v1.07 起；仅支持电机侧主反馈，不支持负载侧第二反馈参与此整定。
- 获取/许可：© Beckhoff Automation；未发现可整站镜像的开源许可。本汇编保存官方链接和原创摘要，不搬运手册正文。
- 核验：opened，2026-10-17
