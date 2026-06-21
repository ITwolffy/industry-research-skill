---
name: industry-research
description: Use when the user asks to analyze or understand an industry, market, or sector. Triggers on questions about market size, competitive landscape, business model viability, industry trends, or whether a market is worth entering — regardless of motivation (investment, career, entrepreneurship, consulting).
---

# Industry Research Framework

## Overview

A systematic framework for rapidly understanding any industry, derived from 肖璟's *如何快速了解一个行业*. It maps the industry lifecycle to four key analysis dimensions (feasibility, scalability, defensiveness, profitability) and provides concrete analysis tools for each stage.

**Core insight:** Different lifecycle stages demand different analysis priorities. Don't analyze everything equally — weight dimensions by where the industry is in its lifecycle.

## When to Use

Use this skill when:
- The user asks to "analyze", "understand", "research", or "evaluate" an industry, market, or sector
- The user asks about market size, growth potential, competitive dynamics, or business model of a specific industry
- The user is making an investment, career, or business decision that requires industry context
- The user asks "is X industry worth entering" or "what's the outlook for Y sector"

**Do NOT use when:**
- "What's Tesla's market cap?" (single data point, not industry analysis)
- "How many cybersecurity companies are in China?" (fact lookup, not analysis)
- "When was GDPR enacted?" (historical fact)
- The user is already an expert in that specific industry and wants a narrow technical discussion
- The task is pure data gathering — use `deep-research` for extensive fact-collection

**Complementary skills:**
- `deep-research`: Use when extensive fact-collection and source verification is needed
- `brainstorming`: Use before this skill when the user's question is vague or underspecified
- `writing-plans`: Use when the analysis will lead to an implementation plan
- `verification-before-completion`: Use to validate conclusions before presenting final analysis

## Analysis Depth: Pick Your Level

Not every question needs the full framework. Choose the depth before starting:

| Level | When to Use | Scope | Deliverable |
|---|---|---|---|
| **Quick Scan** | Casual question, initial triage, "is this worth looking into?" | Lifecycle stage + rough market size + 2-3 sentence verdict | 1-2 paragraphs |
| **Standard** | Investment decision, career move, business entry | All 5 steps + key data + PEST summary | 5-10 page brief |
| **Deep Dive** | Professional report, due diligence, board presentation | Full framework + valuation + competitors + prosperity indicators | Full report with appendices |

**Signal detection:** If the user says "quickly", "roughly", "at a high level", or asks a yes/no question → Quick Scan. If they ask for "analysis", "report", or "should I invest/enter" → Standard. If they request "comprehensive", "detailed report", or "due diligence" → Deep Dive.

## The Main Framework

### Step 0: Define the Industry Scope

Before analysis, pick a classification standard to avoid "口径不一致":

| Standard | Issuer | Best For |
|---|---|---|
| 《国民经济行业分类》 | 国家统计局 | Macro data alignment, broad industry mapping |
| 《上市公司行业分类指引》 | 中国证监会 | A-share listed company analysis |
| 《申万行业分类标准》 | 申万宏源研究 | Market-standard granular analysis (3-tier: 一级/二级/三级) |
| GICS | MSCI & S&P | Cross-market comparison (US/HK/A-share) |

### Step 1: Determine the Industry Lifecycle Stage

Use **penetration rate** as the primary indicator:

```
1. Find penetration rate data
   ├─ Durable goods (cars, appliances)? → Use NEW SALES penetration (monthly sales %)
   └─ Consumable/service (software, SaaS)? → Use STOCK penetration (% of user base)
2. Map to stage:
   ├─ < 15-20%   → 导入期 (Import)     → Focus: Feasibility
   ├─ 15-40%     → 成长期 (Growth)     → Focus: Scalability
   ├─ > 35-40%   → 成熟期 (Maturity)   → Focus: Defensiveness + Profitability
   └─ Declining  → 衰退期 (Decline)    → Focus: Substitutes / Second curve
```

Note: thresholds are empirical guides from historical data (e.g., smartphones crossed 20% in 2010), not rigid rules. Adjust for industry specifics.

**Why penetration rate works:** It maps to Rogers' Innovation Diffusion Theory — industries grow as products move through user segments: innovators → early adopters → early majority → late majority → laggards. The 15-20% threshold signals the early majority entering (the "takeoff" point), and 35-40% signals the late majority arriving (growth deceleration).

**Caveat — real curves are messier:** Real industries don't follow smooth S-curves. Revenue fluctuates around the trend (e.g., masks spiked during COVID but didn't enter a true growth stage). Short-term supply-demand mismatches can disguise as lifecycle transitions. Always triangulate penetration rate with other signals (e.g., are multiple firms consistently profitable? Is the business model validated?).

### Step 2: Apply the Four Analysis Dimensions

Weight each dimension based on the lifecycle stage:

#### A. Feasibility (导入期 focus) — "Can this business model work?"

**Start here — map the business model first.** Before judging feasibility, use a Business Model Canvas (商业模式画布) to understand what the industry actually does: value proposition, customer segments, channels, revenue streams, key resources, key partners, cost structure. Fill it from industry reports. Only then assess feasibility.

**Sales feasibility** — Is demand real?
- **Time benchmarking:** What past need does this satisfy with a new solution? (Successful models usually satisfy existing needs in new ways, not create new needs)
- **Space benchmarking:** Has this model succeeded in mature markets? (Cross-market comparison)

**How capital validates models in practice:**
- **调研法 (Survey method):** FMCG-style market research — questionnaires, focus groups, observational studies. Tests demand before large investment.
- **试错法 (Trial-and-error):** Let entrepreneurs figure it out. VC logic: "下注于赛道，而非赛手" (bet on the track, not the rider). If the industry is a real opportunity, multiple teams trying different approaches will eventually find what works.

**Profit feasibility** — Can it make money?
- **Qualitative:** Assess revenue (frequency × elasticity of demand) + cost (standardization level)
  - Profit = Revenue - Cost
  - Revenue: Must have either high frequency OR low elasticity
  - Cost: Higher standardization → lower costs but harder to charge premium
- **Quantitative:** Build a Unit Economics (UE) model
  - Find the minimum operating unit (one store, one order, one product)
  - Model revenue, costs, profit for that unit
  - If one unit can't be profitable, scaling won't help
  - Build 3 versions: current state, breakeven, end-state

**Business models that can't charge users directly (无法收费的商业模式):**

Some models (e.g., WeChat, search engines, social media) can't easily charge end users despite satisfying high-frequency, low-elasticity needs. Instead, they monetize indirectly — advertisers or merchants pay, and users "pay" with attention/data. For these models, assess ARPU (Average Revenue Per User):
- How much can advertisers/merchants earn from each user?
- What percentage of that are they willing to spend on customer acquisition?
- This becomes the implicit revenue per user.

These models are hard to value in import/growth stages (easy to be over-optimistic). The 2015 internet bubble was largely caused by over-estimating monetization potential for user-heavy, revenue-light platforms.

**Innovation Hierarchy — is the underlying tech mature enough?**

A viable-looking business model can fail because foundational technology isn't ready. Innovation flows bottom-up:

```
  应用层 (Application)  ← Business model innovation (e.g., ride-hailing app)
  中间层 (Middleware)   ← OS/platform innovation (e.g., iOS/Android)
  基础层 (Foundation)   ← Infrastructure innovation (e.g., 4G/5G, batteries)
```

Before assessing business model viability, check: has the prerequisite technology layer matured? Example: pre-2015 EVs failed not because demand was fake, but because battery energy density (基础层) wasn't sufficient — the whole application layer was propped up by subsidies.

**Red flags for feasibility:**
- Satisfying a need that never existed before (without strong evidence)
- Low frequency + high elasticity (worst combination)
- Unit economics permanently negative with no path to breakeven
- **Underlying foundational technology not yet mature** (the most common silent killer)

#### B. Scalability (成长期 focus) — "How big can this get?"

**Three market size definitions:**
| Type | Definition | When to use |
|---|---|---|
| TAM (Total Addressable Market) | Potential demand if fully saturated | Import stage (can it support IPOs?) |
| SAM (Served Available Market) | Currently satisfied demand | Growth stage (how much room left?) |
| SOM (Served Obtainable Market) | What one company captures | Maturity stage (market share) |

**Estimation methods — choose based on available data:**

| Method | Best For | Data Needed | When to Use |
|---|---|---|---|
| **Demand-side** | TAM, consumer markets | Target users, penetration %, order volume, unit price | Most common; use when user/customer data is accessible |
| **Supply-side** | SOM, capacity-constrained | Bottleneck identification, max output per unit | Use when supply constraints are the binding factor |
| **Supply-demand matching** | Mature/saturated markets | A stable ratio (e.g., ATMs per capita, doctors per 1000 people) | Only when supply ≈ demand (mature market) AND the ratio is demonstrably stable |

**Demand-side formula:** Target Customers × Penetration Rate × Order Volume × Unit Price
**Supply-side approach:** Find bottleneck → calculate max output per unit → multiply by number of units
**Supply-demand matching:** "以大见小" (top-down) or "以小见大" (bottom-up) using stable per-capita ratios

**Key check:** Can the industry TAM support companies large enough to go public? (< 30B yuan TAM is a red flag for many VCs)

#### C. Defensiveness (成熟期 focus) — "Can it resist substitutes?"

Two ways to build a moat:

**Resource Monopoly (control production factors):**
| Factor | Moats |
|---|---|
| Labor | Star talent (entertainment), entrepreneurs (equity incentives) |
| Land | Natural resources (minerals, climate), location advantage |
| Capital | High entry barriers, economies of scale |
| Technology | Patents, copyrights, trade secrets, know-how |
| Data | Training data moats, user data accumulation |

**Network Effects (control production relationships):**
| Relationship | Moats |
|---|---|
| Government | Licenses, permits, regulatory approvals |
| Peers | Industry standards, price alliances |
| Suppliers | Exclusive supply agreements, bargaining power |
| Customers | Brand (reduces decision cost), channels (controls access), switching costs |

**Key insight — capital can bypass other moats:** Money can hire away star talent, buy land with resource advantages, acquire technology through M&A. The only truly durable moats are those that money alone cannot replicate: government-granted monopolies (licenses), network effects at scale, and data moats accumulated over time. When analyzing moats, always ask: "Could a well-funded competitor buy their way past this?"

**Key insight — the customer-side triad:** Brand + channels + switching costs work together:
- Brand → reduces decision cost (customers default to you)
- Channels → reduces purchase cost (you're where customers are)
- Switching costs → must exceed the value gap vs competitors (otherwise customers leave)

#### D. Profitability (成熟期 focus) — "Who captures the value?"

**Horizontal analysis (among competitors):**

| CR8 Range | Market Structure | Valuation Implication |
|---|---|---|
| 0-40% | Competitive | Growth-stage companies get premium |
| 40-70% | Oligopolistic | Market share gains drive valuation |
| 70-100% | Highly concentrated | Stable P/E, leader premium possible |

**Capacity cycle (4 phases) — the full narrative:**

The cycle progresses through three expansion stages before peaking:

| Stage | Who expands | Signal | Danger level |
|---|---|---|---|
| 被动扩产 | Leader (passive) | Add capacity to meet existing demand | Low |
| 主动扩产 | Leader (active) | Confident expansion based on growth outlook | Medium |
| 无序扩产 | **Outsiders flood in** | Non-industry players enter, seeing easy money | **High — near peak** |

This leads to the 4-phase cycle:
1. **Undersupply** → high utilization, rising prices → leaders passively expand
2. **Surge** → outsiders flood in (无序扩产) → oversupply risk builds rapidly
3. **Clearing** → players exit, analysts turn bearish → weak hands eliminated
4. **Improvement** → supply tightens, margins recover → leaders consolidate share

**Cycle position indicators:**
- CAPEX ÷ Depreciation < 1.5 suggests near bottom (limited new investment)
- CAPEX ÷ Depreciation < 1.0 means **zero** new investment (strong bottom signal)
- Outsiders entering the industry signals approaching peak

**Inventory cycle (库存周期) — a shorter companion cycle:**

| Phase | Signal | What's happening |
|---|---|---|
| 主动补库存 | Firms optimistic, actively building inventory | Demand still strong |
| 被动补库存 | Demand slows, inventory piles up | **Warning: oversupply** |
| 主动去库存 | Firms discount, clear inventory | Price pressure |
| 被动去库存 | Demand recovers, inventory depletes | **Recovery signal** |

Inventory reaching historical highs = danger; hitting historical lows = either undersupply or bottoming.

**Two patterns that break the standard cycle:**

1. **龙头逆势扩张 (Leaders expand against the cycle):** Demand is falling, but the leader expands anyway — backed by government financing or capital market access. Goal: build scale advantage that crushes competitors when the cycle turns. Common in strategic industries (semiconductors, EVs).

2. **龙头主动打价格战 (Leaders initiate price wars):** Demand is fine, but the leader starts a price war to force out smaller players. Seen in 2000s air conditioning (格力/美的 crushed 100+ competitors) and 2022-2023 EVs (Tesla's price cuts). After the war, concentration rises sharply and survivors' margins recover.

**Vertical analysis (along the value chain):**
- Profit distribution determined by: Bargaining willingness × Bargaining power
- Willingness: Value share in downstream cost + lifecycle stage
- Power: Industry concentration + supply-demand tightness
- Track: Gross margin trends across the chain + ability to occupy upstream/downstream funds

**Chain position indicators (from financial statements):**

| Signal | Accounting Item | Direction | Meaning |
|---|---|---|---|
| Occupying upstream | 应付账款 (Accounts Payable) | ↑ Rising | Delaying supplier payment = strong bargaining |
| Occupying downstream | 预收账款/合同负债 (Advances/Contract Liabilities) | ↑ Rising | Customers prepay = strong position |
| Squeezed by upstream | 预付账款 (Prepayments) | ↑ Rising | Must prepay suppliers = weak position |
| Squeezed by downstream | 应收账款 (Accounts Receivable) | ↑ Rising | Customers delay payment = weak position |

### Step 3: Valuation Context

**Valuation is determined by both supply (assets) and demand (investors):**

| Side | Factor | What to watch |
|---|---|---|
| **Investors (demand)** | Capability (钱多不多) | Monetary policy — M1 growth, interest rate direction, liquidity |
| **Investors (demand)** | Willingness (敢不敢买) | Risk appetite — investor confidence surveys, trading volume |
| **Asset (supply)** | 赔率 (Odds) | How big is the upside? (Scale + profitability improvement potential) |
| **Asset (supply)** | 概率 (Probability) | How likely is success? (Feasibility + defensiveness strength) |

**估值由供需双方决定:** Investor capability (money supply) + investor willingness (risk appetite) + asset odds (upside potential) + asset probability (likelihood of success).

**Critical concept — 预期差 (Expectation Gap):** Markets trade on gaps between expectations and reality, not on absolute outcomes. Stocks fall *before* the economy actually worsens (when expectations turn), and rise *before* conditions improve (when pessimism peaks). Always compare your research conclusions against current market consensus, not against the status quo.

**By lifecycle stage:**
| Stage | Valuation driver | Typical P/E |
|---|---|---|
| Import | "Dream" — potential TAM, theme investing | Very high, "市梦率" |
| Growth (early) | Growth surprise, constant estimate beats | 80-120× |
| Growth (late) | Deceleration, estimates harder to beat | 40-80× |
| Maturity | Stable, "leader premium" possible | 20-40× or lower |
| Decline | Low unless supply contraction > demand contraction | Minimal |

**Key metrics to watch:**
- Transaction crowding (换手率, 成交额占比 above 45% of A股 = danger)
- Relative valuation = Industry P/E ÷ Market P/E

### Step 4: External Factors (PEST)

**Political — a gradient of intervention:**

*Supportive policies (from weakest to strongest):*

| Level | Type | Impact | Example |
|---|---|---|---|
| 1 | 口头鼓励 | Minimal — signals direction only | "鼓励发展XX产业" |
| 2 | 补贴减税 | Strong — attracts capital, lowers cost | EV purchase subsidies, tax holidays |
| 3 | 直接投资 | Very strong — creates direct demand | Infrastructure, SOE procurement |
| 4 | 强制使用 | Maximum — mandates adoption | 国六排放标准 OBD, 卫星定位装置 |

*Restrictive policies:*

| Type | What it limits | Example |
|---|---|---|
| 限制准入 | Who can enter | Financial licenses, media permits, 环评 |
| 限制供给 | How much can be produced | Capacity caps for coal/steel/cement |
| 限制价格 | At what price | Coal prices for power, drug集采 pricing |
| 限制受众 | Who can consume | Gaming curfew for minors, alcohol/tobacco age limits |

*International:* US monetary policy + foreign policy (sanctions, tariffs, supply chain restrictions).

**Economic — "量" (quantity) and "价" (price):**

*Quantity indicators:* GDP growth rate, income growth, debt ratios — these drive aggregate demand.

*Price — the three prices of money (货币的三种价格):*

| Price | What it measures | Affects |
|---|---|---|
| 货币购买力 (CPI/PPI) | What goods cost in money | Revenue for food/commodity industries; industries with pricing power benefit from moderate inflation |
| 利率 (Interest rate) | Cost of borrowing money | Valuation (rates ↑ = P/E ↓); capital-intensive industries' financing costs; saver vs borrower behavior |
| 汇率 (Exchange rate) | Price of money in foreign currency | Export competitiveness (CNY ↓ = exports ↑); import costs; foreign capital flows into/out of A-shares |

**Social-cultural:**

- Demographics: aging → healthcare demand ↑; shrinking workforce → automation ↑; "工程师红利" → advanced manufacturing competitiveness
- Cultural shifts: health consciousness → sugar-free beverages; 国潮 → domestic brand premium; environmental awareness → EV adoption
- Track both gradual shifts (demographics) and sudden changes (events that reshape behavior)

**Technological:**
- Technology maturity level (refer to Gartner hype cycle)? Enabling or threatening the industry?
- Does the innovation enable a new business model, reduce costs, or create new distribution channels?
- Innovation flows bottom-up (基础层→中间层→应用层) — check if all prerequisite layers are ready.

### Step 5: Prosperity Tracking (景气度)

**Two approaches to find leading indicators:**
1. **Supply chain approach:** Identify the core driving link in the chain → its indicators lead the whole chain
2. **Key industry indicators:**
   - Upstream materials: Price + inventory
   - Midstream manufacturing: Production/sales volume
   - Consumer staples: CPI/inflation
   - Consumer discretionary: Real estate cycle
   - Services: Macro indicators

**Indicators must be:** Reflective of fundamentals + high-frequency updatable (monthly/weekly/daily)

**Example — 白酒行业景气度 (most iconic case):**

The白酒 industry shows how a single core indicator can drive an entire sector's stock performance. 飞天茅台批价 (wholesale price) correlated ~0.95 with 茅台 stock price (2017-2021).

*Why批价 works as a core indicator:*
- Data available daily (微信公众号 "今日酒价"), no need to wait for quarterly reports
- 批价 directly drives company earnings: it determines 出厂价 ceiling, enables "计划外供货" at higher prices, and signals brand strength
- 批价 cascades through the value chain: 高端批价 sets the ceiling for 次高端, which sets the ceiling for 中端

*Supporting indicators for cross-verification:*
| Indicator | What it reveals | Data source |
|---|---|---|
| 经销商库存 | Oversupply risk; > historical avg = danger | 草根调研 / 券商电话会 |
| 经销商打款情况 | Channel confidence (real money votes) | 草根调研 |
| 开瓶率 | Real consumption vs speculative hoarding | 草根调研 |

*The key lesson:* Indicators can conflict (批价 up but inventory also up). When they do, dig into the logic behind each — don't just average the signals. Understand *why* they're diverging.

## Research Methodology

### Why Research Creates Value — Three Information Gaps (三种信息差)

Research generates investment edge through three types of information asymmetry:

| Gap Type | Definition | Accessibility | Sustainability |
|---|---|---|---|
| **时间差 (Time gap)** | Get information faster than others | Requires privileged access (satellite imagery, crawlers, on-the-ground monitoring) | Low — hard for individuals |
| **广度差 (Breadth gap)** | Know about more fields (Munger's Lollapalooza) | Easy to attempt, hard to do well | Medium — risks FOMO and shallow analysis |
| **深度差 (Depth gap)** | Understand more deeply than others | Open to everyone willing to put in the work | **High — the only sustainable edge** |

**Key insight:** 深度差 is the only reliable path to consistent excess returns for individual researchers. Time gap is institution-dominated; breadth gap without depth leads to "FOMO" without conviction. Build depth in one sector first, then expand breadth.

### DIKW Model — Understanding Research Depth

Research transforms raw data up the value chain:

| Level | Name | Question Answered | Example |
|---|---|---|---|
| D | **Data** | Raw facts | "CPI this month is 2.5%" |
| I | **Information** | What pattern? | "CPI has been above 2% for 5 consecutive months" |
| K | **Knowledge** | What to do? (Know-how) | "Historically, sustained CPI > 2% leads to tightening → reduce growth stock exposure" |
| W | **Wisdom** | Why? (Know-why) | "Tightening raises discount rates, which hits long-duration growth assets hardest" |

**Critical rule:** 事实判断 (Fact judgment — what IS) comes before 价值判断 (Value judgment — what SHOULD be done). Always verify facts before forming opinions. When reading others' analysis, separate their facts from their opinions — use their facts, question their opinions unless backed by clear logic and evidence.

### How These Methods Integrate with the Framework

| Method | Applied in | Purpose |
|---|---|---|
| Hypothesis-driven | Steps 2-5 | Before searching for data, state your hypothesis — then seek confirming/disconfirming evidence |
| Pyramid Principle | After data gathering | Build the logic pyramid: facts → patterns → insights → core conclusion |
| SCQR Framework | Final output | Structure the deliverable: S (context) → C (change) → Q (question) → R (verdict) |

### Hypothesis-Driven Research (for Steps 2-5)

**Avoid boiling the ocean.** For each dimension (feasibility, scalability, etc.), don't search blindly:
1. **Make a hypothesis** (e.g., "this industry's TAM likely exceeds 100B yuan because...")
2. **Decompose** into sub-hypotheses following MECE (Mutually Exclusive, Collectively Exhaustive)
3. **Verify** each sub-hypothesis with specific indicators — search for data that confirms OR disproves

### Pyramid Principle (for synthesizing findings)

Build a logic pyramid bottom-up AFTER gathering data:
1. List all facts/data
2. Group related facts → find patterns
3. Extract key insights per group — **always ask "So what?"** to move from summarizing to distilling
4. Synthesize a single core conclusion at the top

### SCQR Framework (for presenting the final output)

> **Note:** SCQR structures your **deliverable** to an audience. The **analysis itself** follows the 5-step framework above. Use SCQR to wrap the framework's findings into a compelling narrative.

| Element | Meaning | Chinese Analogy |
|---|---|---|
| Situation | Current context | 空 (sky) |
| Complication | What changed | 雨 (rain) |
| Question | Problem raised | 湿 (wet) |
| Resolution | Solution/answer (your 5-step conclusion) | 伞 (umbrella) |

**Adapt SCQR order to audience:**
- **Strangers** (low awareness): C→Q→S→R (lead with conflict to grab attention)
- **Audience** (some interest): S→C→Q→R (classic)
- **Boss** (time-pressed): R→S→C→Q (conclusion first)
- **Direct manager** (already informed): R only

## Quick Application Checklist

Steps 1-8 are the analysis engine; steps 9-10 are synthesis and delivery.

> **Iterative note:** Steps 2-6 are interdependent — you'll often discover market size data (step 4) while determining the lifecycle stage (step 2), or realize the lifecycle stage differs from your initial judgment after analyzing the competitive landscape (step 6). This is normal. Adjust earlier conclusions as new data emerges.

**For Quick Scan:** Do steps 1, 2, 4 (rough TAM only), and jump to 9-10.
**For Standard:** All 10 steps.
**For Deep Dive:** All 10 steps + financial modeling + competitor deep-dives + prosperity dashboard.

1. [ ] Define the industry scope (pick a classification standard; identify key chain links)
2. [ ] Determine penetration rate → identify lifecycle stage (revisit after steps 3-6)
3. [ ] Analyze the primary dimension for that stage (feasibility/scalability/defensiveness/profitability)
4. [ ] Size the market (TAM for import, SAM for growth, SOM for maturity)
5. [ ] Identify moats (resource monopoly + network effects)
6. [ ] Map the value chain and profit distribution (horizontal CRn + vertical margin analysis)
7. [ ] Run PEST analysis for external drivers and headwinds
8. [ ] Identify 2-3 key prosperity indicators for ongoing tracking
9. [ ] Synthesize using Pyramid Principle (facts → patterns → insights → core conclusion)
10. [ ] Present using SCQR framework adapted to audience and depth level

## Report Template

For Standard and Deep Dive analyses, structure your output as:

```
# [Industry Name] 行业分析报告

## 一、核心结论 (SCQR: S→C→Q→R)
## 二、行业定义与范围
## 三、产业生命周期判断 (渗透率 + 阶段定位)
## 四、商业模式可行性 (对标 + UE模型)
## 五、市场规模 (TAM/SAM/SOM)
## 六、护城河分析 (资源垄断 + 网络效应)
## 七、竞争格局与盈利性 (横向CRn + 纵向价值链)
## 八、估值特征 (当前阶段定位)
## 九、外部因素 PEST
## 十、景气度指标体系
## 十一、风险提示
```

## Red Flags — STOP and Reassess

If you find yourself thinking any of these, you're likely misapplying the framework:

| Red Flag Thought | Reality |
|---|---|
| "I'll just skip the penetration rate — it's hard to find" | Wrong lifecycle stage → entire analysis path is wrong |
| "This industry is small, no need to check competitive landscape" | Some import-stage industries (e.g., bike sharing) have price wars early |
| "The business model seems fine, I don't need to verify demand" | The #1 reason import-stage industries fail is pseudo-demand |
| "I can just summarize the data without deeper analysis" | Summarizing ≠ distilling. Always ask "So what?" |
| "Let me analyze all dimensions equally to be thorough" | Even-weighting = missing what matters. Weight by lifecycle stage. |
| "The market size data from one source looks good enough" | Cross-verify. Single-source data is a major risk. |

**All of these mean: Stop. Return to the framework. Apply the correct step.**

## Common Mistakes

| Mistake | Why It Happens | Fix |
|---|---|---|
| Using stock penetration for durable goods | Intuitive to check ownership % | Use new sales penetration for products with 10yr+ replacement cycles |
| Even-weighting all dimensions | "Be thorough" instinct | Weight by lifecycle stage — import stage is 80% about feasibility |
| Summarizing instead of distilling | Confusing reorganization with insight | After each conclusion, ask "So what?" at least once |
| Ignoring external factors | Tunnel vision on industry internals | Always run PEST before finalizing — policies can kill viable models |
| Single data source | First source looks authoritative | Cross-verify key data from at least 2 independent sources |
| Treating penetration thresholds as rigid | "The book says 15-20%" | Thresholds are empirical guides, not rules. Adjust for industry specifics |
| Over-relying on one expert's view | Experts have narrow perspectives | Triangulate: experts + data + cross-market comparisons

## Key Formulas

```
Penetration Rate = Existing Users ÷ Potential Customer Base
Market Size (Demand-side) = Target Customers × Penetration × Order Volume × Unit Price
Capacity Utilization = Actual Output ÷ Maximum Capacity
Relative Valuation = Industry P/E ÷ Market P/E
UE Profit = Unit Revenue - Unit Cost (at minimum operating unit)
```

## Supporting References

- **[Research Tools](references/research-tools.md):** Detailed data sources, search engine techniques, expert network guidance, report filtering strategies, and AI research tools from the book's Part 4.
