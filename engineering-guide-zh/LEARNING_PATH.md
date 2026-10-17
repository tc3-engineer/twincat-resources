# 六阶段学习路线

面向已能独立编写 ST 和调试设备的工程师。以下为整理建议，不是厂商规定课程；按验收成果推进，不要求一次重构整机。

| 阶段 | 优先资料 | 应形成的成果 |
|---|---|---|
| 1. 明确扫描与模块边界 | [A08](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12081376523.html) [A09](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12050040971.html) [A11](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/12081664011.html) [M01](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70043531.html) | 一页调用顺序图；列清请求、接受、执行、完成、故障和输出写入者 |
| 2. 建立可暂停流程 | [A04](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/100978955.html) [A12](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1335919755.html) [A13](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1335962123.html) [A14](https://infosys.beckhoff.com/content/1033/tcplclib_tc3_packml_v2/1336429067.html) [A21](https://stefanhenneken.net/2018/11/17/iec-61131-3-the-state-pattern/) | 用一个独立模块比较 CASE 与状态模式；写明暂停、恢复、停止、复位的转移条件 |
| 3. 以证据定位故障 | [D01](https://infosys.beckhoff.com/content/1033/tc3_grundlagen/6828869003.html) [D10](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/6884133515.html) [D14](https://infosys.beckhoff.com/content/1033/tc3_eventlogger/4278578443.html?id=2759979561564329345) [D17](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/6192246155.html) [D18](https://infosys.beckhoff.com/content/1033/te13xx_tc3_scopeview/182291083.html) | 一份故障记录模板、一份 Scope 配置；保存触发前后证据并能重现时间链 |
| 4. 理解运动边界 | [M01](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70043531.html) [M06](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_mc2/70099339.html) [M10](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/6961172235.html) [M11](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1002438027.html) [M14](https://infosys.beckhoff.com/content/1033/tf5050_tc3_nc_camming/1003655819.html) [M18](https://infosys.beckhoff.com/content/1033/tc3ncerrcode/513147659.html) | 在虚拟轴/离线数据上解释耦合条件、切表连续性和模坐标回绕 |
| 5. 拆开实时与非实时任务 | [I01](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407705867.html) [I02](https://infosys.beckhoff.com/content/1033/tc3_ads.net/9407534859.html) [I10](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_utilities/35419787.html) [I11](https://infosys.beckhoff.com/content/1033/tcplclib_tc2_system/30986763.html) [R10](https://infosys.beckhoff.com/content/1033/tf4100_tc3_controller_toolbox/245435787.html) | 确定 ADS 服务边界、日志缓冲策略、参数单位及控制周期；测量写入负载 |
| 6. 建立小步回归 | [O01](https://github.com/tcunit/TcUnit) [O07](https://github.com/sagatowski/TcStaticAnalysisLoader) [O08](https://github.com/JustusRijke/TcBuild) [R13](https://infosys.beckhoff.com/content/1033/te1200_tc3_plcstaticanalysis/3471332747.html) [R14](https://infosys.beckhoff.com/content/1033/tc3_plc_intro/2527107467.html) | 选择一个纯逻辑函数或状态机测试；固定依赖；保存可回滚提交和构建记录 |

不要从“选最复杂框架”开始。先用一个模块验证暂停/单步、命令握手、故障恢复和可测量性，再决定哪些模式值得扩展。

中文入口优先 [R03](https://tr.beckhoff.com.cn/)；系统化作者课程参考 [A26](https://alltwincat.com/twincat-3-tutorial/)。课程、文章与示例适合建立理解，具体接口仍回到当前官方文档和本地库声明。
