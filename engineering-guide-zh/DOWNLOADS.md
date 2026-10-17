# 获取源码与官方资料

已为 10 个开源项目固定提交，并逐项核对该提交的 LICENSE。源码通过 Git submodule 关联；本目录不是所有上游文件的实体镜像。

## 完整取回源码

在已安装 Git 的电脑执行：

```powershell
git clone --recurse-submodules https://github.com/tc3-engineer/twincat-resources.git
```

已有本仓库时，在仓库根目录执行：

```powershell
git submodule update --init --recursive
```

只需要一个项目时，可指定 `.gitmodules` 中的路径，避免一次下载全部项目。GitHub 的 Download ZIP 不包含子模块源码；上面 Git 命令才会取回这些源码。固定的上游提交将被 checkout，不会自动跟踪上游最新版本。

## 固定版本清单

| 项目 | 提交 | 许可证 | 使用边界 |
|---|---|---|---|
| [Beckhoff-USA-Community/SPT-Libraries](https://github.com/Beckhoff-USA-Community/SPT-Libraries) | [`f598024bfe1c`](https://github.com/Beckhoff-USA-Community/SPT-Libraries/tree/f598024bfe1cbbbca808f36958914b8497119191) | [MIT](https://github.com/Beckhoff-USA-Community/SPT-Libraries/blob/f598024bfe1cbbbca808f36958914b8497119191/LICENSE) | 美国团队社区支持库；当前 V4 对应 4026/PackML V3。 |
| [Beckhoff-USA-Community/SPT_V4_Samples](https://github.com/Beckhoff-USA-Community/SPT_V4_Samples) | [`470ce0f0acc2`](https://github.com/Beckhoff-USA-Community/SPT_V4_Samples/tree/470ce0f0acc28ac16e5237a60fb8259e9c456722) | [0BSD](https://github.com/Beckhoff-USA-Community/SPT_V4_Samples/blob/470ce0f0acc28ac16e5237a60fb8259e9c456722/LICENSE) | 与 SPT V4 配套示例；旧 VFFS Demo 要求不同库版本。 |
| [Beckhoff/ADS](https://github.com/Beckhoff/ADS) | [`24e598a113ed`](https://github.com/Beckhoff/ADS/tree/24e598a113edfdc0d34414bfefb847930d94cb87) | [MIT](https://github.com/Beckhoff/ADS/blob/24e598a113edfdc0d34414bfefb847930d94cb87/LICENSE) | 官方 AdsLib；C/C++ ADS 客户端，不是 PLC 程序架构。 |
| [Beckhoff/TF6000_ADS_DOTNET_V5_Samples](https://github.com/Beckhoff/TF6000_ADS_DOTNET_V5_Samples) | [`89e2de2d2df8`](https://github.com/Beckhoff/TF6000_ADS_DOTNET_V5_Samples/tree/89e2de2d2df82514b91ca8d84705810cebda3515) | [0BSD](https://github.com/Beckhoff/TF6000_ADS_DOTNET_V5_Samples/blob/89e2de2d2df82514b91ca8d84705810cebda3515/LICENSE.md) | 仓库名称含 V5，当前说明为 V6 示例；勿与 V7 API 混用。 |
| [bengeisler/TcLog](https://github.com/bengeisler/TcLog) | [`44a3fe3b6165`](https://github.com/bengeisler/TcLog/tree/44a3fe3b6165fbee66fe7b80dac63e65f9bcab56) | [MIT](https://github.com/bengeisler/TcLog/blob/44a3fe3b6165fbee66fe7b80dac63e65f9bcab56/LICENSE) | 日志库参考；实际 PLC 周期和存储开销自行测量。 |
| [Inxton/TcOpen](https://github.com/Inxton/TcOpen) | [`0397cf08160c`](https://github.com/Inxton/TcOpen/tree/0397cf08160cd82f00c2f4712cf2c56f66641dfd) | [MIT](https://github.com/Inxton/TcOpen/blob/0397cf08160cd82f00c2f4712cf2c56f66641dfd/LICENSE) | 当前仅为 Inxton 内部需求维护；非活跃社区扩展。IVF 等依赖许可另行核对。 |
| [JustusRijke/TcBuild](https://github.com/JustusRijke/TcBuild) | [`71cabcef5af8`](https://github.com/JustusRijke/TcBuild/tree/71cabcef5af8548bff9a148c32a218d92ce4009b) | [MIT](https://github.com/JustusRijke/TcBuild/blob/71cabcef5af8548bff9a148c32a218d92ce4009b/LICENSE) | 作者说明为独立 TwinCAT 4024+/.NET4.8，VS 集成版未测。 |
| [StefanHenneken/Blog-2018-06-IEC61131-StatePattern-Sample03](https://github.com/StefanHenneken/Blog-2018-06-IEC61131-StatePattern-Sample03) | [`e48c21200134`](https://github.com/StefanHenneken/Blog-2018-06-IEC61131-StatePattern-Sample03/tree/e48c21200134eb54e36bf3fb9baeb3d786ac7ce6) | [BSD-2-Clause](https://github.com/StefanHenneken/Blog-2018-06-IEC61131-StatePattern-Sample03/blob/e48c21200134eb54e36bf3fb9baeb3d786ac7ce6/LICENSE) | 作者状态模式示例；用于对照 CASE 与对象状态实现。 |
| [stlehmann/pyads](https://github.com/stlehmann/pyads) | [`716d9a4282fb`](https://github.com/stlehmann/pyads/tree/716d9a4282fb9a19f2c026e4f3ca650593f324b9) | [MIT](https://github.com/stlehmann/pyads/blob/716d9a4282fb9a19f2c026e4f3ca650593f324b9/LICENSE) | Python ADS；适合离线测试与采集，不替代 PLC 实时闭环。 |
| [tcunit/TcUnit](https://github.com/tcunit/TcUnit) | [`425c62939bb8`](https://github.com/tcunit/TcUnit/tree/425c62939bb81810879a244270d47d1b610a3bd3) | [MIT](https://github.com/tcunit/TcUnit/blob/425c62939bb81810879a244270d47d1b610a3bd3/LICENSE) | 稳定但暂停积极开发；测试逻辑仍需目标平台验证。 |

精确提交 SHA 与上游许可证 blob SHA 见 [sources.lock.json](data/sources.lock.json)。本次已核验上游元数据与 LICENSE，未在 TwinCAT/XAE 编译、运行这些工程。

## 官方 PDF 与下载入口

只保存原始链接和原创摘要。下载权限、会员要求和版权由发布方决定。

- [A20 · PackML 官方入口与实施指南](https://www.omac.org/packml)：版权所有；仅收录链接与原创摘要，未确认允许全文再分发
- [I24 · TR3037 Accelerated Troubleshooting 培训大纲](https://www.beckhoff.com/media/downloads/training/baus-training-tr3037-outline-file.pdf)：Beckhoff 版权所有；页面/视频不默认转载；示例代码另按仓库或下载包许可证
- [R01 · 倍福中国下载中心](https://www.beckhoff.com.cn/zh-cn/support/download-finder/)：© Beckhoff Automation；收录链接及原创摘要，未复制手册或视频正文。
- [R03 · 倍福虚拟学院](https://tr.beckhoff.com.cn/)：© Beckhoff Automation；收录链接及原创摘要，未复制手册或视频正文。
