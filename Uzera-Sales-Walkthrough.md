# 🚀 Uzera — Complete Sales Walkthrough

Here's a full breakdown of every key feature on the platform, written so you can confidently explain and demo it to a prospect.

---

## ✨ What Is Uzera?

Uzera is an **AI governance and context layer for software engineering teams**. The core pitch is simple: your AI coding agents (Claude, Cursor, Copilot, Windsurf) are powerful — but they don't know your team's rules, your architecture, or your standards. Uzera fixes that by scanning your codebase, building a live knowledge map, and enforcing your team's rules on every AI-generated edit. **In 5 minutes, your AI agents go from generic to your-company-specific.**

The three things it does:
1. **Scanner maps your code** — deep, structured understanding of every file and function
2. **MCP delivers that knowledge to agents** — any AI tool gets full context automatically
3. **Hooks enforce rules** — violations are blocked *before* code is written, not after review

---

## 🏁 GET STARTED — The Onboarding Flow (7 Steps)

This is your "time to value" story. Uzera promises **5 minutes from zero to working**. Here's how each step maps to a prospect's journey:

**Step 1 – Install the Scanner (~30 seconds)**
One compiled binary, no Node.js required, runs locally. Install with a single terminal command, Homebrew, direct download, or Docker for CI/CD. *Selling point: zero infrastructure commitment, zero DevOps lift to try it.*

**Step 2 – Link Your Repository (~1 minute)**
Creates a single `.uzera-config.json` file (safe to commit). Authentication happens via SSO. *Selling point: no secrets management, no new credentials — fits right into existing workflows.*

**Step 3 – Run Your First Scan (~2 minutes)**
Analyzes code locally using tree-sitter. **Source code never leaves the machine** — only structured metadata uploads to Uzera. Scans ~3,000 files in 6–8 seconds. Extracts 14 structured sections per module (endpoints, DB tables, business rules, auth patterns, etc.). Your Knowledge Tree appears in seconds. *Selling point: privacy-first by design — a major objection killer for enterprise security teams.*

**Step 4 – Adopt Recommended Rules (~1 minute)**
Uzera automatically detects patterns your team already follows at ≥70% consistency and surfaces them as suggested rules. One click to adopt. *Selling point: no manual policy writing. The rules come from what the team already does.*

**Step 5 – Connect Your AI Agent (~30 seconds)**
Works with every MCP-compatible agent. One command per agent:
- `uzera-scanner configure claude-code` → MCP + PreToolUse/PostToolUse hooks + git pre-commit
- `uzera-scanner configure cursor` → MCP + git pre-commit
- `uzera-scanner configure copilot` → git pre-commit
- `uzera-scanner configure windsurf` → MCP + git pre-commit

*Selling point: you're not replacing any existing tool — you're supercharging all of them at once.*

**Step 6 – Enable Sync Advisor (recommended, ~2 minutes)**
Connect your GitHub repo so Uzera can watch main-branch drift, predict merge conflicts, and advise agents before they edit files other branches are already touching. *Selling point: proactive conflict prevention — especially valuable for larger teams.*

**Step 7 – Turn On Brainstorms (Claude Code)**
Opt-in per project. Uzera captures decisions born in Claude Code sessions. Drafts stay private; devs choose what to publish to Team Brainstorms. Agents get recall via `uzera_recall`. *Selling point: institutional memory — decisions made in AI sessions become team-wide knowledge, not lost in chat history.*

**Existing CLAUDE.md / .cursorrules?** There's an import shortcut: Uzera parses existing instruction files and converts them into enforced rules. *Zero disruption for teams already using AI agents.*

---

## 🔍 SCANNER — The Engine Under Everything

The Scanner is the foundation. Everything in Uzera flows from what the Scanner finds. Key points to convey:

**What it does:** It reads your codebase using tree-sitter (a syntax-parsing engine) and extracts **14 structured "sections"** from every module and function. Think of it as building a living spec from code that already exists.

**The 14 sections extracted per module include:**
Endpoints, Data Stores, Business Rules, Security Issues, Input Schemas, Cross-Service Dependencies, Contributors, Architecture, Data Flow, External Services, Cross-Service Calls, Auth Patterns, Rate Limiting, Error Handling, and Observability.

**Why this matters in sales:**
- Agents know *exactly* which endpoints exist, which DB tables are touched, who owns the code, and how it connects to other services — before writing a single line
- Context is always fresh — re-running the scanner (takes seconds) keeps the Knowledge Tree current
- Private by design — only metadata (structure, not source) leaves the machine

**The Scanner also auto-classifies tool side effects** (Read, Write, External Call, Destructive) so that dangerous tools trigger extra review gates automatically — without anyone writing that rule manually.

**ADR recorded decision:** The Scanner binary is compiled with .NET AOT to protect Uzera's IP — no source-code exposure, can't be decompiled. This also means no Node.js runtime dependency for customers.

---

## 🌳 KNOWLEDGE TREE — The Living Codebase Map

The Knowledge Tree is what prospects will *see* in the demo — it's the most visual, impressive part of the product. It has five sub-views:

---

### 📁 Browse Code

The core view. A file tree where every node (module, file, or function) has a **rich knowledge card** showing:
- **Risk Score** (e.g., 87/100 = "High churn · 3 cross-service deps")
- All 14 scanner-extracted sections
- **Annotations** — manual notes attached by team members (e.g., "Idempotency required after incident IR-2024-89")
- **Agent Context tab** — shows exactly what any AI agent sees when it reads this node
- Link to open in GitHub

*Sales angle: engineers can finally see their codebase the way an AI agent sees it — and they can annotate it to add human context that the scanner can't capture.*

---

### 📌 Topics

A structured knowledge base **on top of** the code graph. Teams create and maintain topics across categories:

- **Architecture** — e.g., "Monorepo until 50 devs, service-per-domain after 3 distinct concerns"
- **ADRs (Architecture Decision Records)** — tracked, versioned, tagged, linked to code (e.g., "Scanner must be .NET AOT compiled," "PreToolUse is Claude Code only")
- **Standards** — e.g., "Never refactor without a ticket reference," "Schema changes require architecture review"
- **Strategy** — e.g., "Stripe primary for payments, Adyen for EU expansion 2027"
- **Plans** — e.g., tech debt roadmap with deadlines
- **Policies** — e.g., "Every agent must have a linked eval set with pass-rate threshold"
- **Agent-related** — topics specifically flagged as relevant for AI agent context

Each topic shows contributors, code links, tags, and when it was last updated. Topics can be Pinned, filtered, sorted, and viewed in List or Grid mode.

*Sales angle: this is the "team wiki that agents actually read." Unlike Confluence or Notion, these topics are wired directly into the AI agents' context window.*

---

### ⚠️ Gaps

This is a **demand-signal dashboard** — it shows where your AI agents are hitting dead ends.

**Context Misses** — every time an agent asks for knowledge that doesn't exist in the Knowledge Tree, it's logged here. Examples:
- `payment-retry-policy` requested 5x this week by Claude Code (3x) and Cursor (2x), by devs vipul and sarah
- `api-rate-limiting` requested 3x
- `deployment-process` requested 2x

Each gap shows which agents asked, which developers were involved, when it was last requested, and whether there's a similar existing topic to link to.

**Knowledge Drift** — tracks cases where what agents *are* using no longer matches reality.

**Proactive Suggestions** — AI-powered nudges like "3 agents asked about payment-retry-policy this week — create this topic?" or "billing module has 12 rules but auth has 0 — review suggested rules?"

*Sales angle: Gaps turns your agents into a feedback loop. The more your team uses AI, the better the Knowledge Tree gets. This is a compounding advantage.*

---

### 🗺️ Architecture Map

An **auto-generated visual service graph** derived entirely from scanner data. No manual Miro or Lucidchart needed.

Shows: service nodes, HTTP routes, events, DB dependencies, agent flows, LLM calls, vector stores, and prompt references. Filterable by: HTTP, Event, DB, JWT, LLM, Memory, Prompt.

**Example graph for billing-service:** 16 nodes, 24 edges, 6 services, 3 data stores, 2 external deps, 3 agent flows, 1 LLM provider.

**Cross-Service Flows detected automatically:**
- Receipt delivery: billing → email-service → Postmark
- Webhook logging: webhook-service → billing → ClickHouse
- JWT fan-out: auth → billing + webhook-service

Every node is clickable to see inbound/outbound dependencies, owner, and links into the Knowledge Tree. Coding agents receive this via `uzera_context()` in the architecture field.

*Sales angle: the architecture diagram that teams never have time to keep updated — now auto-maintained, always current, and machine-readable by AI agents.*

---

### 👥 Team

The **ownership and bus factor view** — surfaces human risk in AI-assisted codebases.

Key metrics shown: Bus Factor (currently 1 — one person leaving blocks critical work), Sole-owner modules (13 of 18), At-risk modules (14), Active contributors (4, 1 inactive).

**Why this matters for AI:** When an agent edits a sole-owner module, Uzera **automatically attaches the owner to the review** and flags the knowledge gap. This prevents the scenario where an AI makes changes to code only one person understands — with no human notified.

**Ownership risk levels:**
- **CRITICAL** — sole owner + high criticality, or owner is inactive, or AI-authored prompts with no human reviewer
- **WARN** — single owner, high blast radius, or AI-dominant authorship (e.g., a prompt file where 18 of the last edits were by Claude Code with no human review)
- **OK** — active ownership with multiple contributors

Also covers agentic artifacts: Flows, Prompts, and Evals can be "owned" and at-risk just like regular code.

*Sales angle: this is the governance view that engineering managers and CTOs care about. It's not just about AI writing code — it's about who's accountable for it.*

---

## 🧠 Knowledge Tree — Additional Sub-Sections (Sidebar)

Beyond the five main tabs, the left navigation exposes deeper sub-sections:

**Flows (7)** — Every AI agent flow in the repo, categorized by type: DAG, React Loop, Code Agent, Plan+Execute, Handoff Chain, Swarm, Event-Driven. Each flow shows the framework (LangGraph, OpenAI Agents SDK, etc.), agents involved, source files, and a live graph of nodes and edges.

**Agents (23)** — Every individual agent, sortable by error rate or eval score. Shows role (Worker, Orchestrator, Router, Tool-Caller, Evaluator, Entry, Exit), source file, prompt used, tools available, eval score, 7-day invocation count, and error percentage. Instantly see which agents need attention (e.g., `migrator` at 16% error rate, `draft_response` at 11%).

**Prompts (6)** — All system prompts version-controlled and tracked. Shows token count, variable signatures, version number, which agent uses it, and who last edited it (including "Claude Code" as an editor — triggering ownership flags). *Key governance feature: prompt edits are tracked the same way code edits are.*

**Tools (11)** — Every tool available to agents with side-effect classification (Read, Write, External Call, Destructive). Shows which agents call it, 7-day invocation count, and last failure. Destructive tools automatically trigger gate checks.

**Memory (4 systems)** — Tracks all memory systems in use: Vector (pgvector, 142k chunks), Episodic (mem0, 8.4k sessions), Procedural (Letta, 184 learned skills), and Working (ephemeral, cleared per review). Shows scope (org/user/team), retrieval strategy, and which agents read/write each store.

**Evals (6)** — Offline eval sets linked to agents, run by Braintrust or LangSmith. Shows pass rate vs. threshold and trend. Flags regressions (e.g., `draft_response` at 74% against an 80% threshold — a live issue). *Selling point: evals are first-class artifacts, tied to prompts and agents, not floating in a separate tool.*

**Guardrails (5)** — Runtime validators that run on every inference. Types include: Output Schema validation (Pydantic-AI), PII Redaction (Guardrails-AI), Jailbreak Detection (NeMo), Sandbox Escape Check (custom), and Factuality Checks. On-failure actions: Retry, Block, Escalate, or Log. Shows trigger and failure counts so you can see guardrail effectiveness in real time.

---

## 💡 The Sales Summary (Elevator Pitch Points)

| What a prospect worries about | How Uzera answers it |
|---|---|
| "Our AI agents don't follow our standards" | Scanner extracts your standards from code; Rules enforce them before code is written |
| "We don't want source code leaving our servers" | Only structured metadata uploads — source stays local |
| "It'll take weeks to set up" | 5 minutes, one binary, no Node.js, works with every major AI tool |
| "We use Claude AND Cursor AND Copilot" | One integration, all agents — Uzera sits below all three |
| "We're worried about AI overwriting critical code" | Team view flags sole-owner modules; agents auto-notify owners |
| "How do we know what the AI agents know?" | Knowledge Tree shows exactly what context every agent receives |
| "Prompts and eval sets are unmanaged chaos" | Prompts and Evals are version-controlled, ownership-tracked, and regression-gated |
