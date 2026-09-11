<div align="center">

# Charles

AdTech Engineer · Bidding / High concurrency

[中文](./README.md) · **English**

</div>

---

I build DSP bidding engines, and I write notes.

OpenRTB in, a bid out, a hard `tmax` in the middle. Targeting, frequency caps, pacing, scoring, then Kafka / Flink and online inference — I take the path apart and write until I can explain it.

The notes live at **[cylshao.com](https://cylshao.com)**. About 160 so far.

## Work

- **Bidder**: parse → target → recall → score → bid. Split the latency budget first; optimize after that.
- **Delivery**: frequency capping, budget pacing, how a campaign is compiled and pushed — full or incremental.
- **Serving**: CTR / CVR scoring pulled out of the bidder process into its own high-concurrency service.
- **Lately**: agent loops — tools, memory, eval, resume. Build one by hand, then look at frameworks.

## Writing

Same question throughout: how ads actually run in production.

| | What I write |
| :--- | :--- |
| Ads | OpenRTB, header bidding, App SDK, RTA, consent and attribution |
| Infra | Netty, Kafka, Flink, Redis, availability, Kubernetes |
| Models | Features, recall → rank → re-rank, online inference; agents |

I draw the diagrams. I write the trade-offs. No vendor posts.

## Stack

| | |
| :--- | :--- |
| Languages | Java (primary), Go, C++, Python |
| Ads | OpenRTB, Prebid, RTA |
| Server | Netty, Dubbo, Redis, Kafka, Flink, MySQL |
| Models | PyTorch, ONNX, features and online scoring |
| Deploy | Kubernetes, Grafana |

---

<div align="center">

[cylshao.com](https://cylshao.com)&nbsp;&nbsp;·&nbsp;&nbsp;[LinkedIn](https://www.linkedin.com/in/cylshao/)&nbsp;&nbsp;·&nbsp;&nbsp;[X](https://x.com/cylshao)

charles [at] cylshao.com&nbsp;&nbsp;·&nbsp;&nbsp;UTC+8

If this is useful, I’m happy to talk.

</div>
