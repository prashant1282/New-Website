# Greptile — Competitive Analysis

> **Date:** April 2026
> **Category:** Codebase-aware AI code review agent for pull requests

---

## Company Snapshot

| | |
|---|---|
| **Founded** | 2023 |
| **Total raised** | $30M (incl. $25M Series A) |
| **Valuation** | $180M |
| **Employees** | ~20 |
| **Headquarters** | San Francisco, CA (1664 Larkin Street) |
| **Compliance** | SOC 2 |
| **YC batch** | W24 |

---

## Founders & Leadership

- **Daksh Gupta** — Co-founder & CEO. Georgia Tech CS '23. Went viral in 2024 for his "9-9-6 / 84-hour workweek" hiring pitch; received death threats and a flood of applicants. [LinkedIn](https://www.linkedin.com/in/dakshg)
- **Soohoon Choi** — Co-founder. Georgia Tech CS + Math '23. [LinkedIn](https://www.linkedin.com/in/soohoonchoi/)
- **Vaishant Kameswaran** — Co-founder. Georgia Tech CS.

---

## Funding History

| Round | Amount | Date | Lead Investor(s) |
|---|---|---|---|
| Seed | $4M | 2024 | Initialized Capital (post-YC W24) |
| Series A | $25M | Sep 2025 | Benchmark (Eric Vishria), with Initialized, YC, Cory Levy |

**Total raised:** ~$30M at **$180M valuation**

---

## Key Milestones

- **2023** — Founded after pivoting from "Tabnam" (AI shopping assistant that got YC-rejected)
- **Winter 2024** — Accepted into Y Combinator W24
- **Mar 2024** — Launched on Hacker News: "RAG on codebases that actually works"
- **Oct 2024** — Daksh Gupta's 84-hour workweek post goes viral on X
- **Sep 2025** — $25M Series A + v3 launch for code validation
- **Early 2026** — **v4 release**: confidence scoring, 74% increase in addressed comments/PR, TREX test-generation agent, Greptile MCP server
- **2026** — 500M+ lines reviewed in a single month; 180K+ bugs claimed prevented

---

## Product & Core Features

- **Codebase graph indexing** — dependency graph of files, functions, symbols across the whole repo
- **Parallel agent swarm** — multiple agents assess PR impact cross-module
- **Continuous learning** — learns team conventions from past reviewer comments
- **Custom rules** — plain-English standards (via `greptile.json`)
- **TREX** (early access) — autonomous test generation & sandbox execution per PR
- **Confidence scoring** (v4) — each comment tagged with certainty to aid triage
- **Greptile MCP server** — exposes review data to Claude Code, Cursor, Codex, Devin

---

## ICP & Notable Customers

**Ideal Customer Profile:** Mid-market to enterprise engineering teams on GitHub/GitLab who can't afford missed bugs and have discipline to triage noise. Best-fit: complex multi-module codebases where changes cascade.

**Clients:** Brex, Whoop, Substack, Klaviyo, Zapier, Joby, PostHog, WorkOS, Browserbase, Retool, Bilt, Podium, Gumloop, Y Combinator internal team — **9,000+ teams total**

**Flagship case:** Brex ships **30% faster** with Greptile

---

## Pricing Model

| Tier | Price | Details |
|---|---|---|
| **Cloud** | $30/developer/month | 50 reviews included · $1/review overage |
| **Free tier** | $0 | Qualified OSS projects only |
| **Startup discount** | Custom | Pre-Series A companies |
| **Enterprise** | Custom annual contract | Self-hosted on AWS · bring-your-own-LLM · SSO · SOC 2 |

**Trial:** 14-day free trial
**GTM:** Bottom-up PLG via GitHub App → enterprise sales

---

## Social & Activity

| Channel | Status |
|---|---|
| **Twitter/X** | Highly active — Daksh Gupta (@dakshgup) is a viral-tier founder voice |
| **LinkedIn** | Active company page — weekly customer spotlights (Podium, Gumloop, etc.) |
| **Blog** | greptile.com/blog — technical releases (v3, v4), benchmarks |
| **Hacker News** | Launch thread (Mar 2024) hit front page; team responds to criticism directly |
| **YC** | W24 alumni profile still drives top-of-funnel |

---

## Competitors & Positioning

| Competitor | Positioning vs. Greptile |
|---|---|
| **CodeRabbit** | #1 direct rival; larger user base, lower false-positive rate (2 vs 11/run in benchmarks), leaner comments |
| **Graphite Agent** | PR-platform-native; caught only 6% bugs vs Greptile's 82% in third-party benchmark |
| **Cursor Bugbot** | In-editor AI review from Cursor |
| **Bito** | PR merge acceleration, 87% human-grade feedback claim |
| **Panto AI, CodeAnt, Qodo** | Emerging challengers |
| **GitHub Copilot PR reviews** | Incumbent bundled option |

**Positioning:** The **highest-recall AI reviewer** ("catches 3x more bugs, merge 4x faster") built on full-graph codebase context vs. diff-only tools.

---

## Unique Selling Points

1. **Whole-codebase graph over diff-only review** — catches multi-file logical bugs (NVIDIA/Netflix/Meta public examples) that diff-scoped tools miss
2. **Highest third-party bug-catch rate in the category** — 82% vs CodeRabbit 44%, Cursor 58%, Graphite 6%
3. **Singular focus on review (not generation)** — intentional product bet: "nobody wants a flaky code-review robot"; reliability-first positioning
4. **Agent-interop via MCP** — Greptile becomes the review substrate for Claude Code, Cursor, Devin agents instead of competing with them

---

## Negative Feedback (Hacker News, Reddit, Community)

- **High false-positive rate** — third-party benchmarks show ~11 false positives/run vs CodeRabbit's 2; reviewers note it "requires a mature team to manage effectively" (source: Panto AI, Techsy benchmark analyses, 2026)
- **Trust/honesty incidents** — Hacker News users accused Greptile of misleading marketing-chart claims and misrepresenting self-hosting availability ("tied to enterprise plan... they're still lying"). One thread characterized them as "utter YC trash with no real customers"
- **Founder/culture controversy** — Daksh Gupta's 2024 viral "84-hour workweek, no work-life balance" post drew death threats and polarized the developer community; some engineers refuse to evaluate the product on principle
- **Noise vs. precision tradeoff** — higher comment volume can overwhelm PR authors; addressed-comment rate was only 30% pre-v4 (now 43% post-v4 per Greptile's own metrics) — still below ideal
- **Tiny team (~20) vs. Series A scope** — capacity questions around enterprise support, especially given aggressive land-and-expand into Brex/Klaviyo-scale accounts

---

## Sources

- [Greptile pricing page](https://www.greptile.com/pricing)
- [Greptile v4 launch blog](https://www.greptile.com/blog/greptile-v4)
- [Benchmark Series A — TechCrunch, Jul 2025](https://techcrunch.com/2025/07/18/benchmark-in-talks-to-lead-series-a-for-greptile-valuing-ai-code-reviewer-at-180m-sources-say/)
- [$25M Series A close — SiliconANGLE, Sep 2025](https://siliconangle.com/2025/09/23/greptile-bags-25m-funding-take-coderabbit-graphite-ai-code-validation/)
- [Georgia Tech News — Jan 2026](https://news.gatech.edu/news/2026/01/05/y-combinator-backing-and-30m-investment-take-startup-greptile-next-level)
- [Initialized founder spotlight](https://blog.initialized.com/2024/10/founder-spotlight-greptiles-daksh-gupta/)
- [YC company profile](https://www.ycombinator.com/companies/greptile)
- [Inc — viral 80-hour workweek](https://www.inc.com/sam-blum/this-22-year-old-tech-ceo-says-an-80-hour-work-week-is-a-lifestyle-choice-it-earned-him-death-threats-and-job-seekers/91022060)
- [HN thread — AI code review bubble](https://news.ycombinator.com/item?id=46766961)
- [Panto AI — Greptile vs CodeRabbit benchmark](https://www.getpanto.ai/blog/coderabbit-vs-greptile-ai-code-review-tools-compared)
- [Techsy benchmark — Best AI code review 2026](https://techsy.io/blog/best-ai-code-review-tools)
- [Sacra analysis](https://sacra.com/c/greptile/)
- [Oden comparison — CodeRabbit vs Bugbot vs Greptile vs Graphite](https://getoden.com/blog/coderabbit-vs-cursor-bugbot-vs-greptile-vs-graphite-agent)
