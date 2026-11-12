<div align="center">

# Charles

**Ad tech engineer** · DSP bidding · High-throughput, low-latency systems · AI agents

<sub>[English](#about)&nbsp;&nbsp;·&nbsp;&nbsp;[中文](#more-languages)&nbsp;&nbsp;·&nbsp;&nbsp;[日本語](#more-languages)&nbsp;&nbsp;·&nbsp;&nbsp;[한국어](#more-languages)&nbsp;&nbsp;·&nbsp;&nbsp;[Español](#more-languages)</sub>

</div>

---

## About

I'm an engineer in programmatic advertising. Beyond the code, I care a lot about the business itself: what the demand and supply sides each want, how an impression opportunity is traded through real-time bidding (RTB), and how revenue is split among the DSP, ad exchange, SSP and publisher. Once you understand the business, most system design decisions make sense.

I currently work on DSP bidding, with peak traffic of around 1 million QPS. Every OpenRTB bid request must be answered within its `tmax`, and after the network round trip the DSP typically has only 10–30 ms of processing time. Within that budget it runs targeting filters, frequency capping, budget pacing, online CTR/CVR prediction and bid calculation. Outside the request path, impression and click events stream back through Kafka and Flink to update budget spend, frequency counters and model features.

I write about all of this at **[cylshao.com](https://cylshao.com)**, about 160 posts so far (in Chinese).

## Currently exploring: AI agents

I've spent a good part of this year on AI agents, and I use Cursor for day-to-day development. What interests me is which tasks agents can take over in the business, such as data extraction, data reconciliation, or a first pass over the metrics when a campaign behaves oddly. None of this is complicated, but it's hard to write down as fixed rules, so it has always been done by hand.

My sense is that results depend more on whether data, processes and permissions are in order than on which underlying model you pick. Next, I'll try a few of these tasks in ad tech and write up what works and what doesn't.

## What I write about

The posts cover the areas below. They all come back to the same question: how traffic is monetized, and how the systems in between work.

| Area | Topics |
| :--- | :--- |
| **Ads** | Programmatic ecosystem and impression flow · Header bidding · Bid shading · ads.txt and schain · IAB TCF · MMP / SKAN attribution |
| **Bidding** | Bidder architecture · Bitmap inverted index for targeting · Campaign config snapshots · Frequency capping · PID-based budget pacing |
| **Infra** | Kafka reliability and exactly-once · Flink backpressure and checkpointing · Netty tuning · Redis high availability · Rate limiting, circuit breaking and degradation |
| **Models** | Feature engineering · Retrieval → pre-ranking → ranking → re-ranking · Offline evaluation · Inference serving: selection and rollout |
| **Agents** | Agent loop · Tool design and write-operation safeguards · Context and memory · Checkpoint-based interrupt and resume · Trajectory-level evaluation |

> Posts are drafted by me, proofread with AI assistance, and finalized by hand. Each one takes real effort, so if you spot a mistake, please let me know.

<br />

---

## More languages

<details>
<summary><b>中文</b></summary>

<br />

### 关于我

我在做程序化广告的研发。除了写代码，我也比较关注业务本身：需求方和供给方各自要什么，一次曝光机会如何通过实时竞价（RTB）成交，收入又如何在 DSP、ADX、SSP 和媒体之间分配。业务理解清楚了，很多系统为什么这样设计也就好理解了。

目前主要负责 DSP 竞价，系统峰值 QPS 约 100 万。每个 OpenRTB Bid Request 都必须在 `tmax` 限定的时间内返回 Bid Response，扣除网络往返后，留给 DSP 内部处理的通常只有 10–30 毫秒。这段时间里要完成定向过滤、频次控制、预算平滑（pacing）、CTR/CVR 在线预估和出价计算；请求链路之外，曝光、点击等事件经 Kafka、Flink 实时回流，用于更新预算消耗、频次计数和模型特征。

这几年写的文章都放在 **[cylshao.com](https://cylshao.com)** 上，目前约 160 篇。

### 最近在看：AI Agent

今年花在 AI Agent 上的时间比较多，平时开发也在用 Cursor。我更关心 Agent 在业务里能接下哪些活，比如数据提取、数据核对，或者投放异常时先做一轮指标排查。这些事情不复杂，但很难写成固定规则，一直靠人工来做。

我的感觉是，效果好不好，更多取决于数据、流程和权限有没有梳理清楚，而不是换哪个底层模型。接下来会在广告业务里挑这类场景试一试，有收获或者踩了坑，都会写到博客上。

### 在写什么

文章大致分下面几个方向，说到底都在讲：流量怎么变现，系统在中间怎么运转。

| 方向 | 主题 |
| :--- | :--- |
| **广告** | 程序化生态与曝光流转 · Header Bidding · Bid Shading · ads.txt 与 schain · IAB TCF · MMP / SKAN 归因 |
| **竞价** | Bidder 架构 · 位图倒排定向索引 · 投放配置快照下发 · 频次控制 · 基于 PID 的预算平滑 |
| **基建** | Kafka 可靠性与 Exactly-Once · Flink 反压与 Checkpoint · Netty 调优 · Redis 高可用 · 限流、熔断与降级 |
| **模型** | 特征工程 · 召回 → 粗排 → 精排 → 重排 · 离线评估 · 推理服务选型与发布 |
| **Agent** | Agent Loop · 工具设计与写操作防护 · 上下文与记忆 · Checkpoint 中断续跑 · 轨迹级评测 |

> 文章由我起草，AI 辅助校对，最后手动定稿。每篇都花了不少时间，发现错误欢迎指出。

</details>

<details>
<summary><b>日本語</b></summary>

<br />

### プロフィール

プログラマティック広告の開発をしています。コードを書くだけでなく、ビジネスそのものにも関心があります。需要側と供給側がそれぞれ何を求めているのか、1 回のインプレッション機会がリアルタイム入札（RTB）でどのように取引されるのか、収益が DSP・アドエクスチェンジ・SSP・媒体の間でどう分配されるのか。ビジネスを理解すると、システムがなぜそう設計されているのかも見えてきます。

現在は主に DSP の入札を担当しており、システムのピーク QPS は約 100 万です。OpenRTB の Bid Request には `tmax` で定められた時間内に Bid Response を返す必要があり、ネットワークの往復時間を除くと、DSP 内部で使える処理時間は通常 10〜30 ミリ秒しかありません。その間にターゲティングによるフィルタリング、フリークエンシーキャップ、予算ペーシング、CTR/CVR のオンライン予測、入札額の計算を行います。リクエスト経路の外では、インプレッションやクリックなどのイベントが Kafka と Flink を通じてリアルタイムに戻り、予算消化、フリークエンシーカウンター、モデル特徴量の更新に使われます。

これまでに書いた記事は **[cylshao.com](https://cylshao.com)** にまとめており、現在約 160 本です（中国語）。

### 最近取り組んでいること：AI エージェント

今年は AI エージェントに多くの時間を使っており、普段の開発でも Cursor を使っています。関心があるのは、エージェントが業務の中でどんな仕事を引き受けられるかです。たとえばデータ抽出やデータの突き合わせ、配信に異常があったときの一次的な指標調査などです。どれも複雑ではありませんが、固定のルールに落とし込むのが難しく、これまでずっと人手で行われてきました。

成果を左右するのは、どの基盤モデルを選ぶかよりも、データ・業務フロー・権限が整理されているかどうかだと感じています。今後は広告業務の中でこうした場面を選んで試し、うまくいったことも、つまずいたこともブログに書いていくつもりです。

### 書いていること

記事はおおむね以下の分野に分かれます。突き詰めれば、トラフィックがどう収益に変わるのか、その間でシステムがどう動いているのか、という同じテーマです。

| 分野 | トピック |
| :--- | :--- |
| **広告** | プログラマティック広告のエコシステムとインプレッションの流れ · Header Bidding · Bid Shading · ads.txt と schain · IAB TCF · MMP / SKAN アトリビューション |
| **入札** | Bidder アーキテクチャ · ビットマップ転置インデックスによるターゲティング · 配信設定のスナップショット配布 · フリークエンシーキャップ · PID 制御による予算ペーシング |
| **インフラ** | Kafka の信頼性と Exactly-Once · Flink のバックプレッシャーと Checkpoint · Netty のチューニング · Redis の高可用性 · レート制限、サーキットブレーカー、縮退運転 |
| **モデル** | 特徴量エンジニアリング · リトリーバル → 粗ランキング → ランキング → リランキング · オフライン評価 · 推論サービングの選定とリリース |
| **エージェント** | エージェントループ · ツール設計と書き込み操作の保護 · コンテキストとメモリ · Checkpoint による中断と再開 · 軌跡レベルの評価 |

> 記事は私が下書きし、AI で校正したうえで、最後は自分の手で仕上げています。どの記事も時間をかけて書いているので、誤りに気づいたらぜひ教えてください。

</details>

<details>
<summary><b>한국어</b></summary>

<br />

### 소개

프로그래매틱 광고 개발을 하고 있습니다. 코드를 작성하는 것 외에도 비즈니스 자체에 관심이 많습니다. 수요 측과 공급 측이 각각 무엇을 원하는지, 하나의 노출 기회가 실시간 입찰(RTB)을 통해 어떻게 거래되는지, 수익이 DSP, 애드 익스체인지, SSP, 매체 사이에서 어떻게 배분되는지 같은 것들입니다. 비즈니스를 이해하면 시스템이 왜 그렇게 설계되었는지도 자연스럽게 보입니다.

현재는 주로 DSP 입찰을 담당하고 있으며, 시스템의 피크 QPS는 약 100만입니다. 모든 OpenRTB Bid Request는 `tmax`로 정해진 시간 안에 Bid Response를 반환해야 하고, 네트워크 왕복 시간을 빼면 DSP 내부에서 쓸 수 있는 처리 시간은 보통 10~30밀리초에 불과합니다. 이 시간 안에 타기팅 필터링, 빈도 제한(frequency capping), 예산 페이싱, CTR/CVR 온라인 예측, 입찰가 계산을 마쳐야 합니다. 요청 경로 밖에서는 노출, 클릭 등의 이벤트가 Kafka와 Flink를 거쳐 실시간으로 돌아와 예산 소진, 빈도 카운터, 모델 피처를 갱신하는 데 쓰입니다.

지금까지 쓴 글은 [cylshao.com](https://cylshao.com)에 모아 두었고, 현재 약 160편입니다(중국어).

### 요즘 관심사: AI 에이전트

올해는 AI 에이전트에 많은 시간을 쓰고 있고, 평소 개발에도 Cursor를 사용합니다. 제가 관심 있는 것은 에이전트가 실제 업무에서 어떤 일을 맡을 수 있는가입니다. 예를 들어 데이터 추출, 데이터 대조, 캠페인에 이상이 생겼을 때의 1차 지표 점검 같은 일입니다. 복잡한 일은 아니지만 고정된 규칙으로 만들기 어려워서 지금까지 계속 사람이 해 왔습니다.

결과는 어떤 기반 모델을 고르느냐보다 데이터, 업무 프로세스, 권한이 잘 정리되어 있는지에 더 크게 좌우된다고 느낍니다. 앞으로 광고 업무에서 이런 작업을 골라 시도해 보고, 잘된 점과 시행착오를 블로그에 정리할 계획입니다.

### 쓰고 있는 글

글은 대체로 아래 분야로 나뉩니다. 결국 모두 같은 질문, 즉 트래픽이 어떻게 수익이 되는지, 그 사이에서 시스템이 어떻게 돌아가는지를 다룹니다.

| 분야 | 주제 |
| :--- | :--- |
| **광고** | 프로그래매틱 생태계와 노출 흐름 · Header Bidding · Bid Shading · ads.txt와 schain · IAB TCF · MMP / SKAN 어트리뷰션 |
| **입찰** | Bidder 아키텍처 · 비트맵 역색인 기반 타기팅 · 캠페인 설정 스냅샷 배포 · 빈도 제한 · PID 기반 예산 페이싱 |
| **인프라** | Kafka 신뢰성과 Exactly-Once · Flink 백프레셔와 Checkpoint · Netty 튜닝 · Redis 고가용성 · 레이트 리미팅, 서킷 브레이커, 서비스 강등(degradation) |
| **모델** | 피처 엔지니어링 · 후보 생성 → 사전 랭킹 → 랭킹 → 리랭킹 · 오프라인 평가 · 추론 서빙 선정과 배포 |
| **에이전트** | 에이전트 루프 · 도구 설계와 쓰기 작업 보호 · 컨텍스트와 메모리 · Checkpoint 기반 중단과 재개 · 궤적 수준 평가 |

> 글은 제가 초안을 쓰고 AI의 도움으로 교정한 뒤, 마지막에는 직접 다듬어 완성합니다. 한 편 한 편 시간을 들여 쓰고 있으니, 오류를 발견하시면 알려 주세요.

</details>

<details>
<summary><b>Español</b></summary>

<br />

### Sobre mí

Soy ingeniero de publicidad programática. Más allá del código, me interesa mucho el negocio en sí: qué buscan la demanda y la oferta, cómo se negocia una oportunidad de impresión mediante pujas en tiempo real (RTB) y cómo se reparten los ingresos entre el DSP, el ad exchange, el SSP y el medio. Cuando se entiende el negocio, la mayoría de las decisiones de diseño de los sistemas cobran sentido.

Actualmente trabajo en el sistema de pujas de un DSP, con un tráfico pico de alrededor de 1 millón de QPS. Cada bid request de OpenRTB debe responderse dentro de su `tmax` y, descontado el tiempo de ida y vuelta por la red, al DSP le quedan normalmente solo entre 10 y 30 ms de procesamiento. En ese margen aplica filtros de segmentación, control de frecuencia, dosificación del presupuesto (pacing), predicción en línea de CTR/CVR y cálculo de la puja. Fuera de la ruta de la solicitud, los eventos de impresión y clic vuelven en tiempo real a través de Kafka y Flink para actualizar el gasto del presupuesto, los contadores de frecuencia y las features de los modelos.

Escribo sobre todo esto en **[cylshao.com](https://cylshao.com)**, con unos 160 artículos hasta ahora (en chino).

### Explorando ahora: agentes de IA

Este año he dedicado buena parte de mi tiempo a los agentes de IA y uso Cursor en el desarrollo diario. Me interesa saber qué tareas del negocio pueden asumir los agentes: extracción y conciliación de datos, o una primera revisión de métricas cuando una campaña se comporta de forma anómala. Nada de esto es complicado, pero es difícil plasmarlo en reglas fijas, así que siempre se ha hecho a mano.

Mi impresión es que los resultados dependen más de que los datos, los procesos y los permisos estén en orden que del modelo base que se elija. Lo próximo será probar algunas de estas tareas en ad tech y escribir sobre lo que funciona y lo que no.

### Sobre qué escribo

Los artículos cubren las áreas siguientes. Todos vuelven a la misma pregunta: cómo se monetiza el tráfico y cómo funcionan los sistemas que hay en medio.

| Área | Temas |
| :--- | :--- |
| **Publicidad** | Ecosistema programático y flujo de una impresión · Header bidding · Bid shading · ads.txt y schain · IAB TCF · Atribución con MMP / SKAN |
| **Pujas** | Arquitectura del bidder · Índice invertido con bitmaps para segmentación · Distribución de snapshots de configuración de campañas · Control de frecuencia · Pacing del presupuesto con control PID |
| **Infraestructura** | Fiabilidad y exactly-once en Kafka · Backpressure y checkpointing en Flink · Ajuste de Netty · Alta disponibilidad en Redis · Limitación de tasa, circuit breaking y degradación controlada |
| **Modelos** | Ingeniería de features · Recuperación → pre-ranking → ranking → re-ranking · Evaluación offline · Inference serving: selección y despliegue |
| **Agentes** | Bucle del agente · Diseño de herramientas y protección de operaciones de escritura · Contexto y memoria · Interrupción y reanudación con checkpoints · Evaluación a nivel de trayectoria |

> Redacto yo cada artículo, lo reviso con ayuda de IA y lo cierro a mano. Cada uno lleva bastante trabajo, así que si encuentras un error, avísame.

</details>

<br />

---

<div align="center">

If you're working on similar things, feel free to reach out.

</div>
