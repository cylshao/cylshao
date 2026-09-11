<div align="center">

# Charles

AdTech Engineer · Bidding / High concurrency

[中文](./README.md) · **English**

</div>

---

I like systems. I care more about the market they sit in — who buys, who sells, how inventory clears, and which millisecond the stack is stuck on.

I build DSP bidders and write the ecosystem and the path side by side. OpenRTB in, a bid out, a hard `tmax` in the middle. Protocols, auctions, SDKs, consent; targeting, caps, pacing, scoring; then Kafka / Flink and online inference. If it is still fuzzy, I write until I can explain it.

If those two sides do not meet, I do not count it as understood. Notes: **[cylshao.com](https://cylshao.com)**. About 160 so far.

## Work

- **Bidder**: parse → target → recall → score → bid. Split the latency budget first; optimize after that.
- **Delivery**: frequency capping, budget pacing, how a campaign is compiled and pushed — full or incremental.
- **Serving**: CTR / CVR scoring pulled out of the bidder process into its own high-concurrency service.
- **Lately**: agent loops — tools, memory, eval, resume. Build one by hand, then look at frameworks.

## Writing

Same question throughout: how traffic turns into revenue, and how the system runs in the middle.

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
