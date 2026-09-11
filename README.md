<div align="center">

# Charles

程序化广告工程师 · 竞价 / 高并发

**中文** · [English](./README.en.md)

</div>

---

技术我喜欢。广告这行我更较真——谁在买、谁在卖、库存怎么成交，系统在中间卡哪一毫秒。

做 DSP 竞价，也把生态和链路拆开写。OpenRTB 进来，出价出去，中间是死的 `tmax`。协议、拍卖、SDK、合规，定向、频控、pacing、打分，后面的 Kafka / Flink、在线推理，想不清楚就写到能跟人讲明白。

两边对不上，就不算懂。笔记在 **[cylshao.com](https://cylshao.com)**，大约 160 篇。

## 工作

- **Bidder**：协议解析 → 定向 → 召回 → 打分 → 出价。先把延迟预算切清楚，再谈优化。
- **投放**：频控、预算 pacing、Campaign 怎么编进线上，改完怎么全量 / 增量发出去。
- **推理**：CTR / CVR 从竞价进程里拆出来，做成单独的高并发服务。
- **最近**：Agent 循环——工具、记忆、评测、续跑。先手搓一遍，再去对照框架。

## 写作

都往同一件事收：流量怎么变成收入，系统在里面怎么跑。

| 方向 | 在写什么 |
| :--- | :--- |
| 广告 | OpenRTB、Header Bidding、App SDK、RTA、合规与归因 |
| 基建 | Netty、Kafka、Flink、Redis、高可用、K8s |
| 模型 | 特征、召回 → 精排 → 重排、在线推理；Agent |

图会自己画。取舍会写出来。不写软文。

## 技术

| | |
| :--- | :--- |
| 语言 | Java（主力）、Go、C++、Python |
| 广告 | OpenRTB、Prebid、RTA |
| 服务 | Netty、Dubbo、Redis、Kafka、Flink、MySQL |
| 模型 | PyTorch、ONNX、特征与在线打分 |
| 部署 | Kubernetes、Grafana |

---

<div align="center">

[cylshao.com](https://cylshao.com)&nbsp;&nbsp;·&nbsp;&nbsp;[LinkedIn](https://www.linkedin.com/in/cylshao/)&nbsp;&nbsp;·&nbsp;&nbsp;[X](https://x.com/cylshao)

charles [at] cylshao.com&nbsp;&nbsp;·&nbsp;&nbsp;UTC+8

如果这些对你有用，欢迎聊。

</div>
