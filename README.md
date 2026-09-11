# Charles

**AdTech Engineer** · Programmatic / Bidding · [cylshao.com](https://cylshao.com)

[English](#english) · [中文](#中文)

---

<a id="english"></a>

## English

Programmatic advertising engineer (~5 years). Build DSP bidding engines and the infra around them — ms-level latency, high QPS, production systems at large request scale.

### Experience highlights

- Led DSP bidder core path and platform infra; grew daily request volume from tens of millions to tens of billions; sustained **99.9%** availability with elastic, self-healing operations
- End-to-end bidding under `tmax`: OpenRTB parse → targeting → recall → score → bid / rank → fill; timeout budgets, circuit breaking, degradation, bulkhead isolation
- Delivery controls: multi-dimension frequency capping, budget pacing (target curve + PID), campaign compile → bitmap inverted index → full / incremental publish
- RTA: ask advertisers before bid with ~5ms budget, cache TTL, fail-open / fail-closed under privacy constraints
- Decoupled model inference from bidder into a high-concurrency serving layer (PyTorch → ONNX, multi-version load, batch scoring); online CTR / CVR with **P99** as the KPI
- Led a 20+ person monetization team through a full commercial loop; evaluate designs by **eCPM / ROAS / cost**, not only “does it run”

### Tech stack

| Area | Skills |
| --- | --- |
| Languages | Java (primary, JVM tuning), Go, C++, Python, Vue 3 / H5 |
| Bidding & protocols | OpenRTB 2.5 / 2.6, RTB / PMP, Header Bidding / Prebid, RTA, schain / SPO |
| Server | Netty, Dubbo, Nacos, Sentinel, Protobuf / gRPC, Caffeine |
| Data & middleware | Redis, MySQL, Kafka, Flume, Flink, Spark, Doris / ClickHouse, InfluxDB |
| ML / serving | PyTorch, ONNX, feature engineering, CTR / CVR online scoring, batch inference |
| Cloud & observability | Kubernetes, Grafana, Jenkins, canary / blue-green, chaos engineering |
| Mobile monetization | Mediation, in-app bidding, rewarded / interstitial formats, MMP / SKAN |

### Writing · [cylshao.com](https://cylshao.com)

~160 essays across three tracks:

| Track | Focus |
| --- | --- |
| A · Ad business & ecosystem | OpenRTB, HB / Prebid, App SDK, RTA, pacing / freq cap, TCF / identity / attribution |
| B · High-concurrency infra | Netty, Kafka, Flink, Redis, HA / resilience, MySQL / OLAP, Dubbo / K8s |
| C · Models & AI apps | Features, recall → rank → re-rank, inference serving; agent loops (tools, memory, eval, LangGraph) |

### Links

[Blog](https://cylshao.com) · [LinkedIn](https://www.linkedin.com/in/cylshao/) · [X](https://x.com/cylshao) · charles [at] cylshao.com

*Asia-Pacific · UTC+8 · EN / 中文*

---

<a id="中文"></a>

## 中文

程序化广告工程师（约 5 年）。做 DSP 竞价引擎与周边基建——毫秒级延迟、高 QPS、大体量请求下的生产系统。

### 工作内容

- 主导 DSP Bidder 核心链路与平台基建；日请求从千万级做到百亿级；可用性稳定在 **99.9%**，可弹性、可自愈
- `tmax` 约束下的端到端竞价：OpenRTB 解析 → 定向 → 召回 → 打分 → 出价 / 排序 → 填充；超时预算、熔断、降级、舱壁隔离
- 投放控制：多维频控、预算 Pacing（目标曲线 + PID）、Campaign 近线编译 → 位图倒排 → 全量 / 增量发布
- RTA：竞价前实时询问广告主，约 5ms 预算、缓存 TTL、fail-open / fail-closed，在隐私约束下用第一方数据影响出价
- 将模型推理从 Bidder 解耦为高并发服务（PyTorch → ONNX、多版本加载、批量打分）；CTR / CVR 在线化，以 **P99** 为链路 KPI
- 带过 20+ 人商业化团队并跑通变现闭环；用 **eCPM / ROAS / 成本** 衡量方案，而不只看「系统能否跑起来」

### 技术栈

| 类别 | 技术 |
| --- | --- |
| 语言 | Java（主力，JVM 调优）、Go、C++、Python、Vue 3 / H5 |
| 竞价与协议 | OpenRTB 2.5 / 2.6、RTB / PMP、Header Bidding / Prebid、RTA、schain / SPO |
| 服务端 | Netty、Dubbo、Nacos、Sentinel、Protobuf / gRPC、Caffeine |
| 数据与中间件 | Redis、MySQL、Kafka、Flume、Flink、Spark、Doris / ClickHouse、InfluxDB |
| 模型与推理 | PyTorch、ONNX、特征工程、CTR / CVR 在线打分、批量推理 |
| 云原生与可观测 | Kubernetes、Grafana、Jenkins、金丝雀 / 蓝绿、混沌工程 |
| 移动变现 | Mediation、In-App Bidding、激励视频 / 插屏等格式、MMP / SKAN |

### 写作 · [cylshao.com](https://cylshao.com)

约 160 篇，三个轨道：

| 轨道 | 内容 |
| --- | --- |
| A · 广告业务与生态 | OpenRTB、HB / Prebid、App SDK、RTA、Pacing / 频控、TCF / 身份 / 归因 |
| B · 高并发工程底座 | Netty、Kafka、Flink、Redis、高可用 / 韧性、MySQL / OLAP、Dubbo / K8s |
| C · 模型工程与 AI | 特征、召回 → 精排 → 重排、推理服务；Agent 循环（工具、记忆、评测、LangGraph） |

### 链接

[博客](https://cylshao.com) · [LinkedIn](https://www.linkedin.com/in/cylshao/) · [X](https://x.com/cylshao) · charles [at] cylshao.com

*亚太 · UTC+8 · 中文 / EN*
