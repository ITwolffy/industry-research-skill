# Research Tools Reference

Practical tools and data sources for industry research, drawn from Chapters 12-13 of *如何快速了解一个行业*.

## Data Sources

### Official Statistical Agencies (China)

**Key central government sources:**
- **国家统计局 (NBS):** All macro data — GDP, CPI, PMI, industrial output, population
- **中国人民银行 (PBoC):** Financial data — money supply, social financing, interest rates
- **财政部 (MOF):** Fiscal data — tax revenue, budget, land sales
- **商务部 (MOFCOM):** Trade data — imports, exports, FDI
- **工业和信息化部 (MIIT):** Industry data by sector — electronics, software, raw materials
- **交通运输部 (MOT):** Transport data — shipping, rail, air, logistics indices
- **农业农村部 (MOA):** Agricultural prices, crop data, livestock

**Financial sector:**
- **中国证监会 (CSRC):** Securities market data, listed company filings
- **国家金融监督管理总局 (NFRA):** Banking and insurance data
- **中国外汇交易中心:** Interest rate benchmarks (LPR, SHIBOR), bond prices
- **中国证券投资基金业协会 (AMAC):** Fund industry AUM, rankings

**Industry associations (selected):**
- **中汽协 / 乘联分会:** Auto industry — monthly sales, inventory
- **中国汽车动力电池产业创新联盟:** Battery production and installation data
- **中国充电联盟:** Charging pile deployment data

### International Sources
- **World Bank:** Cross-country macro data, development indicators
- **IMF:** Economic forecasts, financial stability reports
- **OECD:** Developed economy data, policy analysis
- **IEA:** Energy data — supply, demand, prices, emissions

### Third-Party Research Firms

| Firm | Specialty |
|---|---|
| 艾瑞 (iResearch) | China internet, new economy, 3000+ reports |
| 艾媒 (iiMedia) | New economy, consumer data |
| 克而瑞 (CRIC) | Real estate — monthly sales, daily price indices |
| 七麦数据 (Qimai) | App store analytics, download estimates |
| 窄门餐眼 | Restaurant industry — 30,000+ brand coverage |
| 今日酒价 | Daily liquor wholesale prices |
| 猫眼专业版 | Box office, TV ratings |
| 奥维云网 (AVC) | Home appliance sales data |
| 上海有色网 (SMM) | Non-ferrous metals pricing |
| Euromonitor | Global consumer market data |
| IHS Markit (S&P Global) | PMI, industry forecasts |

## Search Engine Techniques

### Six Key Operators

| Operator | Syntax | Use Case |
|---|---|---|
| Site restrict | `关键词 site:gov.cn` | Search only on government sites |
| File type | `关键词 filetype:pdf` | Find PDF reports only |
| Exact match | `"关键词"` | Match exact phrase (no word splitting) |
| Exclusion | `三体 -动画` | Filter out unwanted results |
| Wildcard | `风口*肖璟` | Fill in forgotten parts of a name/phrase |
| Time range | Use "搜索工具" dropdown | Filter to recent content only |

### Vertical Search Engines
- **i问财:** Financial search — supports conditional queries like "最近三年累计现金分红金额低于最近三年年均净利润30%"
- **Perplexity / 秘塔AI搜索:** AI-powered search with summarization
- **百度学术 / Google Scholar:** Academic papers

## Expert Networks

### When to Use
- You need non-public information or data cross-verification
- You've already mastered the basics via public sources (don't waste expert time on fundamentals)
- You need critical assumptions for market size or market share calculations

### Platforms
- **Paid (expensive, 1000+ RMB/hr):** 凯盛融英 (Capvision), 商霖华通 (BCC), GLG (Gerson Lehrman Group), Third Bridge (高临)
- **Budget:** 在行 App (果壳) — sometimes a few hundred RMB per session
- **Free:** LinkedIn, industry WeChat groups — direct outreach cuts out the middleman

### Interview Best Practices

1. **Prep:** Review expert's background → define their expertise boundary → draft 10-15 questions for 1 hour
2. **Opening:** Compliment their expertise → state the interview purpose → start with their strongest area to gauge quality
3. **During:** Guide back on topic when they drift → use hypothetical questions to bypass NDAs → ask for factual basis behind every opinion
4. **Common pitfalls:**
   - Don't ask experts to predict the future (they're often too close to see the big picture)
   - Don't accept conclusions without asking for supporting facts and logic
   - Don't use expert networks for classified/sensitive tech industries

## Reading Research Reports

### Report Types (Sell-Side)

| Type | Content | Update Frequency |
|---|---|---|
| 宏观研报 | Economic cycle, liquidity, asset allocation | Weekly/Monthly |
| 策略研报 | Market outlook, sector rotation, themes | Weekly |
| 行业研报 | Industry deep-dive, competitive landscape | As needed |
| 公司研报 | Single company analysis, earnings forecasts | Quarterly/As needed |

### Four Ways to Filter Quality Reports

1. **By popularity:** "近一周热门" / "近一月热门" on research platforms. Simple but subject to clickbait.
2. **By team reputation:** Follow 新财富最佳分析师 award winners. Caveat: not purely merit-based.
3. **By recommendation track record:** 搜狐金罗盘券商研究能力评测 tracks analyst prediction accuracy.
4. **By commission ranking:** Higher 公募分仓收入 → more market trust in research quality.

### Using Reports Efficiently
- **New to a topic:** Read a deep-dive report to learn the analysis framework
- **Need market size:** Borrow estimates from reports, note the data source in chart footnotes
- **Need expectations:** Reports reveal consensus — market trades on expectation gaps
- **Finding data sources:** Check chart footnotes in sector reports to discover new databases

## Generative AI for Research

- **Summarization:** Feed transcripts/reports to LLMs for structured extraction
- **Interview notes:** Use 剪映 or similar for speech-to-text, then LLM to organize
- **Data processing:** Use LLMs to parse and structure semi-structured data
- **Analysis assistance:** Use LLMs to suggest alternative hypotheses or counter-arguments
- **Limitations:** Always verify LLM outputs against primary sources; LLMs can hallucinate data

## Information Quality Checklist

When evaluating any data source, ask:
- Who collected this? (Government > reputable research firm > unknown third party)
- How was it collected? (Survey? Crawler? Administrative records? Panel?)
- What's the definition? (Same-named indicators can have different statistical scopes)
- What's the provider's incentive? (Are they selling something? Do they have bias?)
- Can I cross-verify? (Always have at least 2 independent sources for critical data)
