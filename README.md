# Charles

**AdTech Engineer** · Programmatic / Bidding · [cylshao.com](https://cylshao.com)

**English** · [中文](./README.zh-CN.md)

---

Programmatic advertising engineer (~5 years). Build DSP bidding engines and the infra around them — ms-level latency, high QPS, production systems at large request scale.

## Experience highlights

- Led DSP bidder core path and platform infra; grew daily request volume from tens of millions to tens of billions; sustained **99.9%** availability with elastic, self-healing operations
- End-to-end bidding under `tmax`: OpenRTB parse → targeting → recall → score → bid / rank → fill; timeout budgets, circuit breaking, degradation, bulkhead isolation
- Delivery controls: multi-dimension frequency capping, budget pacing (target curve + PID), campaign compile → bitmap inverted index → full / incremental publish
- RTA: ask advertisers before bid with ~5ms budget, cache TTL, fail-open / fail-closed under privacy constraints
- Decoupled model inference from bidder into a high-concurrency serving layer (PyTorch → ONNX, multi-version load, batch scoring); online CTR / CVR with **P99** as the KPI
- Led a 20+ person monetization team through a full commercial loop; evaluate designs by **eCPM / ROAS / cost**, not only “does it run”

## Tech stack

| Area | Skills |
| --- | --- |
| Languages | Java (primary, JVM tuning), Go, C++, Python, Vue 3 / H5 |
| Bidding & protocols | OpenRTB 2.5 / 2.6, RTB / PMP, Header Bidding / Prebid, RTA, schain / SPO |
| Server | Netty, Dubbo, Nacos, Sentinel, Protobuf / gRPC, Caffeine |
| Data & middleware | Redis, MySQL, Kafka, Flume, Flink, Spark, Doris / ClickHouse, InfluxDB |
| ML / serving | PyTorch, ONNX, feature engineering, CTR / CVR online scoring, batch inference |
| Cloud & observability | Kubernetes, Grafana, Jenkins, canary / blue-green, chaos engineering |
| Mobile monetization | Mediation, in-app bidding, rewarded / interstitial formats, MMP / SKAN |

## Writing · [cylshao.com](https://cylshao.com)

~160 essays across three tracks:

| Track | Focus |
| --- | --- |
| A · Ad business & ecosystem | OpenRTB, HB / Prebid, App SDK, RTA, pacing / freq cap, TCF / identity / attribution |
| B · High-concurrency infra | Netty, Kafka, Flink, Redis, HA / resilience, MySQL / OLAP, Dubbo / K8s |
| C · Models & AI apps | Features, recall → rank → re-rank, inference serving; agent loops (tools, memory, eval, LangGraph) |

## Links

[Blog](https://cylshao.com) · [LinkedIn](https://www.linkedin.com/in/cylshao/) · [X](https://x.com/cylshao) · charles [at] cylshao.com

*Asia-Pacific · UTC+8*
