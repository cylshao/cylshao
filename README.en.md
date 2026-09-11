<div align="center">

# Charles

AdTech Engineer · Bidding / High concurrency

[中文](./README.md) · **English**

</div>

---

I genuinely enjoy the engineering, but what keeps me in advertising is the part that sits in front of it: who is buying, who is selling, how a single impression clears in a few dozen milliseconds, and which path the money takes on its way back. Engineering is the middle of that chain, and if you only watch the middle, a lot of decisions stop making sense.

My day job is DSP bidding. An OpenRTB request comes in, a bid goes out, and a `tmax` that gives you nothing sits in between. Above the path there are protocols, auction rules, SDKs and consent; along it there are targeting, frequency caps, pacing and scoring; behind it there are Kafka, Flink and online inference. Whenever a piece of that is still fuzzy to me, I take it apart and write it up until I can explain it to someone else — when the business story and the latency budget refuse to line up, it usually means I have not understood it yet.

What I write ends up at **[cylshao.com](https://cylshao.com)**, around 160 pieces so far.

## Work

- **Bidder**: parse → target → recall → score → bid. Split the latency budget across the path first, so you know what each stage may spend, and only then argue about optimizing any one of them.
- **Delivery control**: frequency capping, budget pacing, and how campaign configuration is compiled into the running system and published afterwards, in full or incrementally.
- **Model serving**: CTR / CVR scoring pulled out of the bidder process into its own high-concurrency service, so model iteration and bidding stability stop pulling on each other.

## Lately

For the past couple of years I have been spending more of my time on AI agents.

The interesting difference is not whether the model is clever. A chat will hand you a list of steps and do none of them; finishing the work means calling tools on its own, holding state along the way, stopping where a person has to agree, and picking the task back up once they answer.

Inside a company, that is also where things stall — not at the model. Which tools you are willing to hand over, how to keep context from growing without bound, where to stop when something goes wrong, where to resume after an interruption, and what the run actually cost. Those questions rhyme with work I already know: timeout budgets, idempotency, retries, audit trails, showing up again in a new setting. That is why I think this layer is where models will really enter everyday work, and why it is worth doing carefully.

My approach is to skip the frameworks at first and write the loop myself — a layer each for tools, memory, eval, cost and resume — then go back and read something like LangGraph against it, to see which of those layers it folds into its own abstractions.

## Writing

Most of the above turns into essays, grouped into four areas that all ask the same question: how traffic turns into revenue, and how the system runs in the middle.

| Area | What I write |
| :--- | :--- |
| Ads | OpenRTB, header bidding, App SDK, RTA, consent and attribution |
| Infra | Netty, Kafka, Flink, Redis, availability, Kubernetes |
| Models | Features, recall → rank → re-rank, online inference |
| Agents | Loop, tools, memory, eval, resume, and how frameworks map onto those layers |

I draw the diagrams myself, and I write down why a choice was made and what it gave up. No vendor posts.

---

<div align="center">

[cylshao.com](https://cylshao.com)&nbsp;&nbsp;·&nbsp;&nbsp;[LinkedIn](https://www.linkedin.com/in/cylshao/)&nbsp;&nbsp;·&nbsp;&nbsp;[X](https://x.com/cylshao)

charles [at] cylshao.com&nbsp;&nbsp;·&nbsp;&nbsp;UTC+8

If you work on any of this, or the notes were useful, I would be glad to talk.

</div>
