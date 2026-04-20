# Competitive Analysis: CodeGraphContext vs Uzera
> **Date:** April 2026
> **Prepared for:** Uzera Internal Strategy
> **Subject:** CodeGraphContext (CGC) — Direct Competitor Review

---

## 1. What is CodeGraphContext?

CodeGraphContext (CGC) is an open-source MCP server and CLI tool that indexes a local codebase into a **graph database** to provide context to AI assistants and developers.

- **Creator:** Open-source community (GitHub: CodeGraphContext/CodeGraphContext)
- **Type:** Open-source developer tool
- **Pricing:** Free (self-hosted)
- **Primary use:** Give AI agents structural code context via MCP
- **Core tech:** tree-sitter parsing → graph database → MCP server

> "Bridge the gap between deep code graphs and AI context."
> — CodeGraphContext tagline

---

## 2. What Does CGC Actually Do?

| Capability | Details |
|---|---|
| Code indexing | Scans codebase, builds a knowledge graph of components |
| Graph database | Stores relationships between functions, classes, files |
| Call chain tracking | Traces callers and callees across hundreds of files |
| Dependency mapping | Identifies direct and indirect dependencies |
| MCP server | Exposes graph via MCP to AI assistants |
| CLI tool | Developers can query the graph from the terminal |
| Natural language queries | Ask questions about the codebase in plain English |
| Real-time watching | Monitors directory for file changes, keeps graph updated |
| `.cgcignore` support | Ignore specific files/directories (like `.gitignore`) |
| Pre-indexed bundles | Load famous repos instantly with `.cgc` bundles |

---

## 3. Head-to-Head Comparison

| Feature | CodeGraphContext | Uzera |
|---|---|---|
| **Core purpose** | Graph-based code context for AI | Full AI Transformation Intelligence Platform |
| **MCP support** | ✅ Basic MCP server | ✅ 10 dedicated MCP tools |
| **Code scanning** | ✅ tree-sitter based | ✅ tree-sitter based (AST) |
| **Scan speed** | Not disclosed | 3,290 files in 6.8 seconds |
| **Knowledge structure** | Graph database | Knowledge Tree (14 sections per module) |
| **Rule enforcement** | ❌ None | ✅ 309 rules across 24 templates |
| **Hook-based blocking** | ❌ None | ✅ Blocks violations in real time |
| **Security detection** | ❌ None | ✅ Per-module security issues |
| **User intelligence** | ❌ None | ✅ Sessions, heatmaps, analytics, funnels |
| **Churn prediction** | ❌ None | ✅ Built in |
| **Product tours/NPS** | ❌ None | ✅ Built in |
| **Readiness score** | ❌ None | ✅ AI Readiness Score (0–100) |
| **Dashboard** | ❌ CLI only | ✅ Full web dashboard |
| **Multi-tenancy** | ❌ Not applicable | ✅ BLOCKMT-001 enforced |
| **Pricing** | Free (open-source) | Free → $29 → $79/user/mo |
| **Deployment** | Self-hosted only | Cloud + local scan option |
| **Private repos** | ✅ Local (free) | ✅ Local (code never leaves machine) |
| **Language support** | Multi-language | Node.js, .NET, Go, Python (more coming) |
| **Backed by** | Open-source community | Uzera (commercial) |
| **Support** | Community only | Commercial support |
| **Compliance** | ❌ None | ✅ Hook-based compliance enforcement |
| **Agent skills** | ❌ None | ✅ Anthropic Agent Skills support |

---

## 4. Where CGC Wins

### Free and Open Source
- Zero cost — any developer can install and use immediately
- No sign-up, no credit card, no vendor lock-in
- Self-hosted = code never leaves the machine by default

### Graph Database Depth
- Stores relationships in a true graph structure (not just flat metadata)
- Excels at complex call chain tracing across hundreds of files
- Can identify circular dependencies and "god objects" instantly

### Developer-First CLI
- Powerful terminal commands for direct querying
- Feels native to developer workflows
- No browser/dashboard required

### Community Momentum
- Open-source = community contributions
- Growing ecosystem of forks and extensions
- Pre-indexed bundles for famous repos

---

## 5. Where Uzera Wins

### Rule Enforcement (Biggest Differentiator)
```
CGC  → reads and maps your code (passive)
Uzera → blocks bad code from being written (active)

CGC has zero rule enforcement.
Uzera has 309 rules, 24 templates, hook-based blocking.
This is the single biggest gap between the two products.
```

### Structured Knowledge Tree
```
CGC  → graph of relationships (good for tracing)
Uzera → 14 sections per module (good for AI context delivery)

CGC tells AI: "UserService calls PaymentService"
Uzera tells AI: endpoints, DB tables, security issues,
                business rules, input schemas, contributors,
                architecture notes — all structured
```

### User Intelligence
```
CGC  → code context only
Uzera → code + user sessions + heatmaps + funnels
        + NPS surveys + churn prediction

No overlap. CGC will never build this.
This is Uzera's second moat.
```

### Commercial Readiness
```
CGC  → open-source, community support, self-hosted only
Uzera → commercial product, SLA, dashboard, compliance,
        enterprise pricing, onboarding support
```

### AI Readiness Score
```
CGC  → no scoring, no measurement
Uzera → single number (0–100) showing AI readiness
        Updates continuously. Gives teams a shared target.
```

---

## 6. The Core Difference in One Line

```
CGC asks:   "How is this code connected?"
            → For developers understanding architecture

Uzera asks: "What does my AI agent need to write correct code?"
            → For AI agents writing new code safely
```

---

## 7. Threat Assessment

| Dimension | Rating | Notes |
|---|---|---|
| **Overlap with Uzera** | Medium | Both do code scanning + MCP — different depth |
| **Short-term threat** | Low | CGC has no rules engine, no dashboard, no user intelligence |
| **Medium-term threat** | Medium | Community could add rule enforcement features |
| **Long-term threat** | Medium | If a commercial company forks and productises CGC |
| **Pricing threat** | High | Free vs paid is always a competitive pressure |
| **Enterprise threat** | Low | CGC has no compliance, no SLA, no support |

**Overall threat level: MEDIUM-LOW**

---

## 8. Uzera's Moat Against CGC

| Moat | Explanation |
|---|---|
| **Rule enforcement** | 309 rules, hooks, blocking — CGC has nothing here |
| **User intelligence** | Sessions, heatmaps, churn — completely different category |
| **Knowledge Tree structure** | 14 sections vs raw graph — more structured for AI agents |
| **Readiness score** | Measurable, trackable AI readiness — no equivalent in CGC |
| **Commercial support** | Enterprise needs SLA and support — CGC can't offer this |
| **Managed agents** | Anthropic Agent Skills integration — CGC has no roadmap here |

---

## 9. Positioning Uzera Against CGC

If a developer asks: **"We already use CodeGraphContext — why pay for Uzera?"**

| CGC gives you | Uzera adds on top |
|---|---|
| Code graph and relationships | 14 structured sections per module |
| Basic MCP server | 10 purpose-built MCP tools |
| Call chain tracing | Rule enforcement + hook-based blocking |
| CLI queries | Full web dashboard + AI Readiness Score |
| Code context only | Code + user behaviour + churn prediction |
| Free, no support | Commercial, supported, compliant |

> "CGC tells your AI agent how your code is connected.
> Uzera tells your AI agent what it's allowed to do —
> and blocks it when it gets it wrong."

---

## 10. Summary

CodeGraphContext is a **technically impressive open-source tool** with genuine overlap in the code scanning and MCP space. It is a real competitor for developer mindshare and budget — especially because it is free.

However, CGC is a **developer tool**, not a platform. It has no rule enforcement, no user intelligence, no dashboard, no compliance, no readiness scoring, and no commercial support.

Uzera is an **AI Transformation Intelligence Platform**. The gap widens significantly once a company needs rules, governance, user context, and measurable AI readiness — which every enterprise will eventually need.

**The biggest risk CGC poses to Uzera is not feature parity — it is the word "free."**
The response to that is demonstrating that Uzera's rule enforcement and user intelligence
deliver ROI that far exceeds the subscription cost.

---

*Analysis prepared by Uzera Strategy · April 2026*