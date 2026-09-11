# Hi, I'm Charles Shao · 邵彦伦

[English](#english) · [中文](#中文)

AdTech engineer · writing at [cylshao.com](https://cylshao.com)

程序化广告工程师 · 笔记写在 [cylshao.com](https://cylshao.com)

---

<a id="english"></a>

## English

I build and write about the systems that turn traffic into revenue — from OpenRTB bidders under a tight `tmax`, through Kafka / Flink event backbones, to ranking features and agent loops.

About five years in programmatic AdTech. Day job: DSP bidding engines and the infra around them (ms-level latency, high QPS, 99.9% availability at large request scale). Side habit: publish the trade-offs I wish I'd found written down.

### What I write about · [cylshao.com](https://cylshao.com)

Three tracks, one through-line: **how ads actually work in production**.

| Track | Topics |
| --- | --- |
| **A · Ad business & ecosystem** | OpenRTB / RTB & PMP, header bidding & Prebid, App SDK / mediation, RTA, pacing & frequency capping, supply-chain transparency, TCF / identity / attribution |
| **B · High-concurrency infra** | Netty, Kafka, Flink, Redis & caching, HA / rate-limit / resilience, MySQL & OLAP, Dubbo / K8s deployment |
| **C · Model & AI apps** | Feature engineering, recall → rank → re-rank, online inference serving; hand-rolled agent loops (tools, memory, eval, guardrails, LangGraph) |

~160 essays so far — diagrams, production trade-offs, no vendor fluff.

### Focus areas

- **Bidding path** — OpenRTB parse → targeting → recall → score → bid, under a hard latency budget
- **Event backbone** — Kafka / Flume / Flink for billing, features, pacing, and anti-fraud
- **Model serving** — CTR/CVR inference decoupled from the bidder (ONNX, batching, P99)
- **Agent engineering** — build the loop yourself first: tools, context/memory, eval, cost & resume; then frameworks

### Elsewhere

- Blog: [cylshao.com](https://cylshao.com)
- LinkedIn: [linkedin.com/in/cylshao](https://www.linkedin.com/in/cylshao/)
- X: [@cylshao](https://x.com/cylshao)
- Mail: charles [at] cylshao.com · charlesshao1024 [at] gmail.com

> Based in Asia (UTC+8). Writing mostly in Chinese with English domain terms; DMs in either language are fine.

---

<a id="中文"></a>

## 中文

我做也写「流量怎么变成收入」这条链路上的系统——从 `tmax` 卡死的 OpenRTB 竞价，到 Kafka / Flink 事件中枢，再到排序特征与 Agent 循环。

程序化广告大约五年。本职是 DSP 竞价引擎与周边基建（毫秒级延迟、高 QPS、大体量请求下 99.9% 可用性）。业余习惯：把当时怎么想的、踩过什么、为什么那样选写下来——网上真正能用的细节往往要么太粗，要么关键处略过了。

### 在写什么 · [cylshao.com](https://cylshao.com)

三个轨道，一条主线：**广告在生产里到底怎么跑**。

| 轨道 | 主题 |
| --- | --- |
| **A · 广告业务与生态** | OpenRTB / RTB·PMP、Header Bidding / Prebid、App SDK / 聚合、RTA、Pacing / 频控、供应链透明度、TCF / 身份 / 归因 |
| **B · 高并发工程底座** | Netty、Kafka、Flink、Redis 与缓存、高可用 / 限流 / 依赖韧性、MySQL 与 OLAP、Dubbo / K8s 部署 |
| **C · 模型工程与 AI 应用** | 特征工程、召回 → 精排 → 重排、在线推理服务；手搓 Agent 循环（工具、记忆、评测、护栏、LangGraph） |

目前约 160 篇——配图、写取舍，不写软文。

### 关注点

- **竞价链路** — OpenRTB 解析 → 定向 → 召回 → 打分 → 出价，死磕延迟预算
- **事件中枢** — Kafka / Flume / Flink 撑计费、特征、pacing、反作弊
- **推理服务** — CTR/CVR 从 Bidder 解耦（ONNX、批量打分、P99）
- **Agent 工程** — 先自己把循环拆开：工具、上下文与记忆、评测、成本与续跑；再对照框架

### 找到我

- 博客：[cylshao.com](https://cylshao.com)
- LinkedIn：[linkedin.com/in/cylshao](https://www.linkedin.com/in/cylshao/)
- X：[@cylshao](https://x.com/cylshao)
- 邮箱：charles [at] cylshao.com · charlesshao1024 [at] gmail.com

> 常驻亚太（UTC+8）。博客以中文为主、保留领域英文术语；中英文私信都可以。

---

> 如切如磋，如琢如磨。
