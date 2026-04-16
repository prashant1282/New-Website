# Uzera vs Sourcegraph — Comparison Sheet

> **Date:** April 2026
> **Purpose:** Internal competitive analysis for positioning, sales enablement, and product gap identification.

---

## Company Overview

| | **Uzera** | **Sourcegraph** |
|---|---|---|
| **Tagline** | Context That Makes AI Work | Code Intelligence Platform |
| **Founded** | Startup stage | 2013 (mature, well-funded) |
| **Core product** | Code Intelligence for AI Agents (PIP) + User Intelligence | Code Search, Navigation, Batch Changes, Cody AI |
| **Primary user** | AI agents (Claude, Cursor, Copilot) | Human developers |
| **Delivery** | MCP server (10 tools) | Web UI, IDE extensions, API |
| **Pricing** | Free / $29 user/mo / $79 user/mo | Free (Cody) / Enterprise (custom) |

---

## Feature-by-Feature Comparison

### Code Intelligence

| Capability | **Uzera** | **Sourcegraph** |
|---|---|---|
| Codebase scanning | AST via tree-sitter | SCIP-based indexing |
| Cross-repo search | Not a primary feature | Core strength — regex, structural, exhaustive search across all repos |
| Code navigation (go-to-def, references) | Not offered | Core feature — precise, cross-repo |
| Knowledge Tree (structured per-module context) | 14 sections per module | Not available |
| Architecture mapping | Auto-detected from scan | Not available |
| Dependency graph (cross-service) | Included in Knowledge Tree | Partial — via code navigation |
| Batch changes (large-scale refactors) | Not available | Core feature — search-and-replace across thousands of repos |
| Code insights (trend analytics) | Not available | Available — track code patterns over time |
| Scan speed | 3,290 files in 6.8s | Indexing-based (not real-time scan; pre-indexed) |

### AI & Agent Support

| Capability | **Uzera** | **Sourcegraph** |
|---|---|---|
| AI-native architecture | Built for AI agents as primary consumer | Built for humans; AI added via Cody |
| MCP server | 10 tools, works with any MCP-compatible agent | Not available |
| Agent Skills (Anthropic ecosystem) | Supported — Claude Managed Agents | Not available |
| Multi-agent support | Claude, Cursor, Copilot, Windsurf, custom | Cody only (proprietary AI assistant) |
| Context delivery to AI | Structured Knowledge Tree via MCP | Cody pulls from Sourcegraph's index internally |
| AI assistant | Not a built-in assistant — feeds external agents | Cody — built-in AI coding assistant |
| AI chat with codebase | Via connected agents (Claude, Cursor) | Cody Chat — native feature |
| AI autocomplete | Not offered (relies on connected agents) | Cody Autocomplete — native feature |

### Rule Enforcement & Governance

| Capability | **Uzera** | **Sourcegraph** |
|---|---|---|
| Coding standards / rules | 309 rules across 24 templates | Not available |
| Rule enforcement (blocking) | Hook-based — blocks violations before commit | Not available |
| Rule templates by language | Node.js, .NET, Go, Python | Not available |
| Compliance support | Yes — rules align with compliance needs | Not a focus |
| Pattern detection | Business tier — detects anti-patterns | Code insights can track patterns but doesn't block them |

### User Intelligence

| Capability | **Uzera** | **Sourcegraph** |
|---|---|---|
| Session replay | Yes | Not available |
| Heatmaps | Yes | Not available |
| Product analytics | Yes | Not available |
| Funnels & journeys | Yes | Not available |
| Product tours | Yes | Not available |
| NPS surveys | Yes | Not available |
| Churn prediction | Yes (Business tier) | Not available |
| Anomaly detection | Yes | Not available |

### Developer Experience

| Capability | **Uzera** | **Sourcegraph** |
|---|---|---|
| Quickstart time | ~5 minutes (npx scanner init → scan → MCP) | Longer — requires deployment, indexing, configuration |
| Self-serve free tier | Yes — permanent, 1 repo | Yes — Cody Free for individuals |
| Web UI / dashboard | Product app (Knowledge Tree, Rules, MCP config) | Full web app (search, navigation, insights, batch changes) |
| IDE integration | Via connected AI agents | Native VS Code and JetBrains extensions |
| API | Yes | Yes (GraphQL API) |
| On-prem / self-hosted | TBD | Yes — core differentiator for enterprises |
| SOC 2 / enterprise compliance | TBD | Yes — mature enterprise security posture |

---

## Gap Analysis

### Gaps in Sourcegraph That Uzera Fills

| # | Gap | How Uzera Fills It |
|---|---|---|
| 1 | **No structured context for AI agents** — Sourcegraph's code intelligence is designed for human consumption (web UI, IDE). AI agents can't easily consume search results. | Uzera delivers a structured Knowledge Tree (14 sections) via MCP, purpose-built for machine consumption. |
| 2 | **No rule enforcement** — Sourcegraph helps you find code but has no mechanism to prevent AI (or humans) from writing code that violates standards. | Uzera provides 309 rules, 24 templates, and hook-based enforcement that blocks violations before they're committed. |
| 3 | **Single-agent lock-in (Cody)** — Sourcegraph's AI features only work through Cody. Teams using Claude, Cursor, or Copilot get no AI-powered code intelligence from Sourcegraph. | Uzera is agent-agnostic. Any MCP-compatible tool gets full context — Claude, Cursor, Copilot, Windsurf, or custom agents. |
| 4 | **No user/product context** — Sourcegraph is purely code-focused. When an AI agent fixes a bug, it has no visibility into which users are affected or what they experienced. | Uzera combines code intelligence with user intelligence — session replay, analytics, heatmaps, churn prediction — giving AI agents the full picture. |
| 5 | **No architecture awareness** — Sourcegraph indexes symbols and references but doesn't produce a holistic view of how modules, services, and data stores relate. | Uzera's Knowledge Tree maps architecture, cross-service dependencies, data stores, business rules, and security issues per module. |
| 6 | **No compliance/governance layer** — Sourcegraph has no opinion on how code should be written. | Uzera provides opinionated, enforceable coding standards aligned to compliance requirements, with language-specific templates. |
| 7 | **No AI Readiness Score** — Sourcegraph doesn't tell you how prepared your codebase is for AI-assisted development. | Uzera's free scan produces an AI Readiness Score, showing gaps AI agents will stumble on. |

### Gaps in Uzera That Sourcegraph Fills

| # | Gap | How Sourcegraph Fills It |
|---|---|---|
| 1 | **No code search** — Uzera scans and structures code but doesn't offer a search interface for developers to query codebases in real-time. | Sourcegraph's core product is exhaustive, cross-repo code search with regex, structural, and symbol-level queries. |
| 2 | **No code navigation** — Uzera doesn't provide go-to-definition, find-references, or cross-repo navigation in a browser or IDE. | Sourcegraph offers precise code navigation across repositories, powered by SCIP indexing. |
| 3 | **No batch changes** — Uzera can't perform large-scale, automated refactors across multiple repositories. | Sourcegraph Batch Changes can find-and-replace patterns across thousands of repos with review workflows. |
| 4 | **No code insights / trend tracking** — Uzera provides a point-in-time scan but doesn't track how code patterns evolve over time. | Sourcegraph Code Insights tracks metrics (e.g., migration progress, tech debt reduction) across the codebase over time. |
| 5 | **No built-in AI assistant** — Uzera feeds context to external agents but doesn't provide its own chat or autocomplete experience. | Cody is a full AI coding assistant with chat, autocomplete, and inline edits, all backed by Sourcegraph's code index. |
| 6 | **No self-hosted / on-prem deployment** — Enterprises with strict data residency requirements may not be able to use Uzera (TBD). | Sourcegraph has mature self-hosted and air-gapped deployment options. |
| 7 | **Less mature enterprise posture** — Uzera is newer and may lack SOC 2, SSO/SAML, audit logs, and other enterprise requirements. | Sourcegraph has years of enterprise deployments with full compliance, SSO, RBAC, and audit capabilities. |
| 8 | **Smaller ecosystem / community** — Uzera is building its user base. | Sourcegraph has a large open-source community, established integrations, and proven scale at Fortune 500 companies. |

---

## Positioning Summary

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   Sourcegraph:  "Help HUMANS find and understand code"          │
│                                                                 │
│   Uzera:        "Help AI AGENTS understand, follow rules,       │
│                  and act on code + user context"                 │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

**They are not direct replacements for each other.** A team could use both:

- **Sourcegraph** for human developers who need to search, navigate, and refactor code
- **Uzera** for AI agents that need structured context, rule enforcement, and user intelligence

The competitive overlap is in the "code intelligence" layer. The strategic question is: **as AI agents do more of the coding, does the developer-facing search UI matter less, and the agent-facing context API matter more?** Uzera bets yes.

---

## When to Choose Which

| Scenario | Recommendation |
|---|---|
| Large eng team needs cross-repo code search | **Sourcegraph** |
| Team adopting AI coding agents (Claude, Cursor, Copilot) and wants them to follow standards | **Uzera** |
| Enterprise needs self-hosted code intelligence with SOC 2 | **Sourcegraph** |
| Team wants AI agents to understand architecture + user behavior | **Uzera** |
| Need large-scale automated refactors across 100+ repos | **Sourcegraph** |
| Need to enforce coding rules and block AI-generated violations | **Uzera** |
| Want a built-in AI chat/autocomplete experience | **Sourcegraph (Cody)** |
| Want to feed context to multiple AI agents via MCP | **Uzera** |
| Need user intelligence (session replay, analytics, churn) alongside code context | **Uzera** |
| Tracking code pattern trends over months/quarters | **Sourcegraph** |
