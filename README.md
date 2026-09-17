# WX

## Agent Experience

WX は、**Agent Experience（AXではなくMX/RX/AX/WX全体）を実際のWorkとして扱うための層**である。

基本の経験型を、

```text
MX → RX → AX → WX → MX → …
```

とする。

> **見つける → 深掘る → 任せる → 生み出す**

---

# 1. Agent Experience の4つの型

### MX — Market X

**発見する**

市場・ユーザー・社会を観察し、何をする価値があるのかを見つける。

```text
Observe
 ↓
Need / Reaction
 ↓
Theme
 ↓
Hypothesis
```

**MX = 見つける**

---

### RX — Research X

**深掘る**

MXで見つけたテーマを調査し、理解・検証・構造化する。

```text
Question
 ↓
Research
 ↓
Analysis
 ↓
Knowledge
 ↓
Method / Hypothesis
```

**RX = 深掘る**

---

### AX — Agent X

**任せる**

RXで得た方法をAgentに渡し、実行可能・反復可能な仕事へ変換する。

```text
Method
 ↓
Agent
 ↓
Tool / Context / Model
 ↓
Automation
 ↓
Repeatable Work
```

AXはAgentそのものではなく、**Agentに仕事を任せ、自動化する経験の層**である。

**AX = 任せる**

---

### WX — Work X

**生み出す**

Agentを含む仕組みを使って、実際の成果物を作り、完成させ、外へ出す。

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

成果物の例：

- 記事
- コード
- 資料
- 作品
- データ
- サービス

**WX = 生み出す**

---

# 2. 基本ループ

```text
        ┌──────────────────────┐
        │                      ↓
MX → RX → AX → WX ────────────┘
│     │     │     │
│     │     │     └─ 生み出す
│     │     └─────── 任せる
│     └───────────── 深掘る
└─────────────────── 見つける
```

### 経験としての問い

| Layer | 問い | 動詞 |
|---|---|---|
| MX | 何をやるべきか？ | 見つける |
| RX | それをどう理解するか？ | 深掘る |
| AX | どこまで任せられるか？ | 任せる |
| WX | 何を生み出すか？ | 生み出す |

WXの成果は再び市場へ出て、MXの観測対象になる。

```text
WX
 ↓
OUTPUT
 ↓
Market / User / Society
 ↓
Reaction / Feedback
 ↓
MX
 ↓
RX
 ↓
AX
 ↓
WX
```

---

# 3. Agent Experience と Engineering

MX / RX / AX / WXを実際に回すためのEngineering側を、DX / AX / AWとして支える。

```text
                 HUMAN / SOCIETY
                       │
                       ▼
                      MX
                 Market X
                       │
                       ▼
                      RX
                Research X
                       │
                       ▼
                      AX
                 Agent X
                       │
                       ▼
                      WX
                  Work X
                       │
                       ▼
                    OUTPUT
                       │
                       └────→ MX
```

Engineering：

```text
DX = Human-facing development environment
AX = Agent execution / delegation environment
AW = Agent workflow definition
```

※ここでは **AX** を「Agent Experienceの略」ではなく、**Agent X / 任せる層**として扱う。Agent Experience全体は **MX → RX → AX → WX** である。

---

# 4. 最小定義

> **MX = 見つける**
>
> **RX = 深掘る**
>
> **AX = 任せる**
>
> **WX = 生み出す**

```text
見つける
  ↓
深掘る
  ↓
任せる
  ↓
生み出す
  ↓
届ける
  ↓
また見つける
```

これは、AIに「書かせる」だけではなく、**何を見つけ、何を研究し、何をAgentに任せ、何を成果として生み出すか**までを含めたAgent Experienceの基本型である。
