# WX

## Work eXecution

WX は、Research で得た知識・仮説を、実際の成果物へ変換する Work 層である。

---

# 1. Core Layers

```text
RX → WX → MX
```

### RX — Research eXploration

**調べる・理解する・仮説を作る**

```text
Question
 ↓
Research
 ↓
Knowledge
 ↓
Hypothesis
```

例：`hoshi-novel`

- コンテスト概要
- 年次・回次
- 応募数
- 入選作品
- 入選者
- 出典URL
- 調査・分析

**RX = 知る**

---

### WX — Work eXecution

**実際に作る・試す・検証する**

```text
Plan
 ↓
Do
 ↓
Check
 ↓
Revise
 ↓
Output
```

例：`hoshi-novel-2026`

- アイデア
- 設定
- 構成
- 草稿
- 推敲
- 完成稿

**WX = やる**

---

### MX — Market eXperience

**市場・ユーザー・社会との関係を観測し、学習する**

```text
Observe
 ↓
Segment
 ↓
Hypothesize
 ↓
Position
 ↓
Communicate
 ↓
Measure
 ↓
Learn
 ↓
Update
```

MXでは、完成したOUTPUTを外部へ出し、フィードバックを作る。

```text
OUTPUT
  ↓
Market
  ↓
Reaction
  ↓
Learning
  ↓
RX / WX
```

**MX = 届けて学ぶ**

---

# 2. Engineering Layers

RX / WX / MXを支える実装側を、

```text
DX → AX → AW
```

として定義する。

### DX — Developer eXperience

**人間がWorkを実行しやすくする環境**

```text
Human
 ↓
DX
 ↓
Tools / API / CLI / UI
 ↓
Work
```

扱うもの：

- Repository
- CLI
- API
- UI
- SDK
- Documentation
- Development workflow
- GitHub
- CI/CD

**DX = 人間の実行環境**

---

### AX — Agent eXecution

**AgentがWorkを実行するためのRuntime**

```text
Goal
 ↓
Agent
 ↓
AX
 ├─ Tool
 ├─ Context
 ├─ Memory
 ├─ Model
 └─ Action
 ↓
Result
```

AXはAgentそのものではなく、**Agentが実際に行動できる実行基盤**として扱う。

**AX = Agentの実行環境**

---

### AW — Agent Workflows

**Agentに何を・どの順番で・どの条件で実行させるか**

```text
Trigger
 ↓
Intent
 ↓
Plan
 ↓
Agent
 ↓
Tools
 ↓
Check
 ↓
Output
```

AWはWorkflow / Orchestration層。

```text
AW
│
├─ Research workflow
├─ Issue workflow
├─ Coding workflow
├─ Review workflow
├─ Release workflow
└─ Publishing workflow
```

**AW = Agentの仕事の設計**

---

# 3. 全体構造

```text
                 HUMAN / SOCIETY
                       │
                       ▼
                      MX
               Market eXperience
                       │
                       │ feedback
                       ▼
                      RX
              Research eXploration
                       │
                       │ knowledge
                       ▼
                      WX
               Work eXecution
                       │
                       │ output
                       ▼
                     OUTPUT
```

これをEngineeringで支える。

```text
                ┌───────────┐
                │    DX     │
                │ Human Dev │
                └─────┬─────┘
                      │
RX ───────────────── WX ───────────────── MX
                      │
                ┌─────▼─────┐
                │    AX     │
                │Agent Exec │
                └─────┬─────┘
                      │
                ┌─────▼─────┐
                │    AW     │
                │ Agent Work│
                └───────────┘
```

# 4. それぞれの問い

| Layer | 問い | 動詞 |
|---|---|---|
| RX | 何が分かるか？ | Research |
| WX | 何を実行するか？ | Work |
| MX | どう届き、どう反応するか？ | Market |
| DX | 人間はどう実行するか？ | Develop |
| AX | Agentはどう実行するか？ | Execute |
| AW | Agentに何をさせるか？ | Workflow |

# 5. WX Decision Gate

RXからWXへ移す判断：

```text
□ 目的が明確か
□ 成果物を定義できるか
□ 小さく始められるか
□ 結果を検証できるか
□ 不確実性は許容範囲か
□ 実行コストに見合う学習価値があるか
□ OUTPUTにつながるか
```

WXからMXへ移す判断：

```text
□ 誰かに届ける必要があるか
□ 利用者・観客・顧客が存在するか
□ 外部反応を観測できるか
□ フィードバックを次のWorkに利用できるか
```

# 6. Repositoryとの対応

```text
RX
├─ research repositories
│
├─ hoshi-novel
│    └─ コンテスト研究
│
└─ research-worldmodel
     └─ 世界モデル研究


WX
├─ production repositories
│
├─ hoshi-novel-2026
│    └─ 小説制作
│
└─ other-work repositories
     └─ 実制作


MX
├─ publishing
├─ audience
├─ market
├─ metrics
└─ feedback
```

一方、

```text
DX
└─ Human-facing development tools

AX
└─ Agent runtime

AW
└─ Agent workflow definitions
```

という関係になる。

# 7. 最小定義

> **RX = 知る**
>
> **WX = やる**
>
> **MX = 届けて学ぶ**
>
> **DX = 人間がやりやすくする**
>
> **AX = Agentが実行できるようにする**
>
> **AW = Agentに仕事をさせる流れを定義する**

この6層によって、

```text
Research
   ↓
Work
   ↓
Market
   ↓
Learning
   ↺
```

を、人間とAgentの両方から実行可能な構造として扱う。
