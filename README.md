# Industry Research — 行业研究框架

A Claude Code skill for rapidly understanding any industry. Derived from 肖璟's *如何快速了解一个行业* (How to Quickly Understand an Industry).

## What This Skill Does

When you ask Claude to analyze an industry, this skill provides a systematic 5-step framework:

1. **Determine lifecycle stage** — using penetration rate + Innovation Diffusion Theory
2. **Assess feasibility** — business model validation, UE economics, innovation hierarchy
3. **Size the market** — TAM/SAM/SOM estimation (demand-side, supply-side, matching)
4. **Evaluate defensiveness** — moat analysis (resource monopoly + network effects)
5. **Analyze profitability** — competitive landscape (horizontal CRn + vertical value chain)

Plus: valuation context by lifecycle stage, PEST external factor analysis, and prosperity indicator tracking.

## Installation

```bash
# Clone to your Claude Code skills directory
mkdir -p ~/.claude/skills
git clone https://github.com/YOUR_USERNAME/industry-research.git ~/.claude/skills/industry-research
```

Or manually:

```bash
mkdir -p ~/.claude/skills/industry-research
cp SKILL.md ~/.claude/skills/industry-research/
cp -r references ~/.claude/skills/industry-research/
```

## Usage

Once installed, Claude will automatically load this skill when you ask questions like:

- "帮我分析一下新能源汽车行业"
- "半导体行业值得投资吗？"
- "Understand the cybersecurity market"
- "Evaluate whether I should enter the fintech space"

You can also explicitly invoke it:

```
/industry-research
```

### Analysis Depth

The skill supports three levels:

| Level | Trigger | Output |
|---|---|---|
| **Quick Scan** | "quickly", "roughly", "at a high level" | 1-2 paragraph verdict |
| **Standard** | "analyze", "report", "should I invest" | 5-10 page brief |
| **Deep Dive** | "comprehensive", "detailed", "due diligence" | Full report with appendices |

## File Structure

```
industry-research/
├── SKILL.md                  # Main skill — the 5-step framework
├── references/
│   └── research-tools.md     # Data sources, search techniques, expert networks, reports
└── README.md                 # This file
```

## About the Source Material

This skill is based on the book *如何快速了解一个行业* by 肖璟 (Xiao Jing), a former McKinsey research analyst and co-founder of the financial education platform 简七理财.

The book provides a comprehensive, practitioner-tested methodology for industry research, drawing from:
- McKinsey's consultant training methodology
- Investment research practices from top Chinese securities firms
- Real case studies across multiple industries

**Book structure** (13 chapters across 4 parts):

| Part | Content | Chapters |
|---|---|---|
| 行研框架篇 | Core framework — lifecycle, feasibility, scalability, defensiveness, profitability, valuation, PEST, prosperity tracking | 1-8 |
| 行研实战篇 | Full application to the new energy vehicle industry | 9 |
| 研究方法篇 | Research methodology — hypothesis-driven, MECE, Pyramid Principle, SCQR framework | 10-11 |
| 研究工具篇 | Research tools — data sources, search engines, expert networks, AI tools | 12-13 |

## Key Concepts

- **Penetration rate** as the primary lifecycle indicator (15-20% = takeoff, 35-40% = deceleration)
- **Four analysis dimensions** weighted by lifecycle stage: feasibility → scalability → defensiveness → profitability
- **Innovation Hierarchy**: Foundation → Middleware → Application layers must mature sequentially
- **Unit Economics (UE) Model**: Validate profit feasibility at minimum operating unit
- **Resource Monopoly + Network Effects**: The two moat-building strategies
- **Capacity Cycle + Inventory Cycle**: Short and medium-term competitive dynamics
- **PEST with intervention gradients**: Political factors range from verbal encouragement to mandatory adoption
- **DIKW Model**: Data → Information → Knowledge → Wisdom
- **Three Information Gaps**: Time gap (institution-dominated), breadth gap (FOMO risk), depth gap (sustainable edge)
- **预期差 (Expectation Gap)**: Markets trade on gaps between expectations and reality

## License

MIT — feel free to use, modify, and distribute.

## Acknowledgments

- 肖璟 (Xiao Jing), author of *如何快速了解一个行业*, for the original methodology
- The Claude Code skills ecosystem

## Contributing

Found a gap or improvement? PRs welcome. This skill was built through three rounds of review against the source material — if you spot something we missed, open an issue.
