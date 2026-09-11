# Charles

**程序化广告工程师** · 竞价 / Ad Serving · [cylshao.com](https://cylshao.com)

[English](./README.md) · **中文**

---

程序化广告工程师（约 5 年）。做 DSP 竞价引擎与周边基建——毫秒级延迟、高 QPS、大体量请求下的生产系统。

## 工作内容

- 主导 DSP Bidder 核心链路与平台基建；日请求从千万级做到百亿级；可用性稳定在 **99.9%**，可弹性、可自愈
- `tmax` 约束下的端到端竞价：OpenRTB 解析 → 定向 → 召回 → 打分 → 出价 / 排序 → 填充；超时预算、熔断、降级、舱壁隔离
- 投放控制：多维频控、预算 Pacing（目标曲线 + PID）、Campaign 近线编译 → 位图倒排 → 全量 / 增量发布
- RTA：竞价前实时询问广告主，约 5ms 预算、缓存 TTL、fail-open / fail-closed，在隐私约束下用第一方数据影响出价
- 将模型推理从 Bidder 解耦为高并发服务（PyTorch → ONNX、多版本加载、批量打分）；CTR / CVR 在线化，以 **P99** 为链路 KPI
- 带过 20+ 人商业化团队并跑通变现闭环；用 **eCPM / ROAS / 成本** 衡量方案，而不只看「系统能否跑起来」

## 技术栈

| 类别 | 技术 |
| --- | --- |
| 语言 | Java（主力，JVM 调优）、Go、C++、Python、Vue 3 / H5 |
| 竞价与协议 | OpenRTB 2.5 / 2.6、RTB / PMP、Header Bidding / Prebid、RTA、schain / SPO |
| 服务端 | Netty、Dubbo、Nacos、Sentinel、Protobuf / gRPC、Caffeine |
| 数据与中间件 | Redis、MySQL、Kafka、Flume、Flink、Spark、Doris / ClickHouse、InfluxDB |
| 模型与推理 | PyTorch、ONNX、特征工程、CTR / CVR 在线打分、批量推理 |
| 云原生与可观测 | Kubernetes、Grafana、Jenkins、金丝雀 / 蓝绿、混沌工程 |
| 移动变现 | Mediation、In-App Bidding、激励视频 / 插屏等格式、MMP / SKAN |

## 写作 · [cylshao.com](https://cylshao.com)

约 160 篇，三个轨道：

| 轨道 | 内容 |
| --- | --- |
| A · 广告业务与生态 | OpenRTB、HB / Prebid、App SDK、RTA、Pacing / 频控、TCF / 身份 / 归因 |
| B · 高并发工程底座 | Netty、Kafka、Flink、Redis、高可用 / 韧性、MySQL / OLAP、Dubbo / K8s |
| C · 模型工程与 AI | 特征、召回 → 精排 → 重排、推理服务；Agent 循环（工具、记忆、评测、LangGraph） |

## 链接

[博客](https://cylshao.com) · [LinkedIn](https://www.linkedin.com/in/cylshao/) · [X](https://x.com/cylshao) · charles [at] cylshao.com

*亚太 · UTC+8*
