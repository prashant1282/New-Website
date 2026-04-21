# Augment Code — Product Features Mindmap

> The Software Agent Company — AI agents that understand your entire codebase.

---

## Flow

**Plan → Implement → Review → Integrate → Scale**

---

## 1. Plan — *Context-Aware Planning*

- Analyzes requests and breaks them into actionable steps before touching code
- Uses the Context Engine to ground plans in real codebase structure
- Surfaces dependencies, architecture patterns, and prior decisions up-front
- Expands short prompts with relevant codebase context automatically
- Supports Ask Mode for read-only exploration without modifications

---

## 2. Implement — *IDE & CLI Agents*

- Executes file edits, terminal commands, and tool calls in one flow
- Runs parallel tool calls to perform multiple operations simultaneously
- Auto Mode plans and implements independently end-to-end
- Works in VS Code, JetBrains IDEs, and directly in the terminal (CLI)
- Understands images — screenshots, mockups, and Figma files
- Performs real-time web search for docs and API references

---

## 3. Review — *Checkpoints & AI Code Review*

- Checkpoint system snapshots state and enables one-click rollback
- AI code reviewer leaves inline GitHub comments like a senior engineer
- Full codebase context applied to every review
- One-click fixes applied directly in the IDE
- Memory review lets you approve or edit agent memories before storage

---

## 4. Integrate — *Tools & Ecosystem*

- Native integrations: GitHub, Linear, Jira, Confluence, Notion, Sentry, Stripe
- MCP integrations: Figma, Stripe, MongoDB, AWS, plus 100+ community tools
- Slack integration for team collaboration (Enterprise)
- Context Engine MCP exposes codebase context to other agents
- Multi-model support — switch between Claude, GPT, and other frontier models
- Rules & Guidelines enforce team coding standards

---

## 5. Scale — *Enterprise Readiness*

- SOC 2 Type II compliance across all tiers
- No training on user data — ever
- SSO, OIDC, and SCIM for enterprise identity management
- CMEK (customer-managed encryption keys) and ISO 42001 compliance (Enterprise)
- Multi-repo support for coordinated changes across repositories
- Scales from side projects to enterprise monorepos (e.g., 3.6M+ LOC)

---

## Mindmap View

```
                        ┌─────────────────┐
                        │  AUGMENT CODE   │
                        └────────┬────────┘
                                 │
      ┌──────────────┬───────────┼───────────┬──────────────┐
      │              │           │           │              │
  1. PLAN      2. IMPLEMENT   3. REVIEW  4. INTEGRATE   5. SCALE
  (Context)    (Agents)       (Review)   (Ecosystem)    (Enterprise)
      │              │           │           │              │
   Prompt+        IDE + CLI    Checkpoints  GitHub        SOC 2
   Ask Mode      Auto Mode    AI Reviewer  Linear/Jira   SSO/SCIM
   Breakdown    Parallel tools Inline PR    MCP 100+      CMEK
   Dependencies Multi-model    Memory edit  Slack         Multi-repo
```

---

## INTENT (Workspace)

### 1. Coordinated Team of Agents

```
Intent — Workspace Product
│
├── 1. Living specification
│   └── Spec stays current as work evolves
│
├── 2. Coordinated agents
│   └── Multiple agents working together on a goal
│
├── 3. Isolated environments
│   └── Each task runs in its own sandboxed workspace
│
└── 4. Parallel task breakdown
    └── Design review and parallel task decomposition
```

---

### 2. Agent Capabilities

```
Agent Capabilities
│
├── Parallel Tool Calls
│   └── Execute multiple operations simultaneously
│
├── Auto Mode
│   └── Independent planning and implementation
│
├── Ask Mode
│   └── Read-only exploration without modifications
│
├── Terminal Execution
│   └── Run npm, git, test commands directly
│
├── Checkpoints
│   └── Snapshot and rollback functionality
│
├── Multi-Model Support
│   └── Switch between Claude, GPT, frontier models
│
├── Multi-Repo Support
│   └── Coordinated changes across repositories
│
├── Image Understanding
│   └── Process screenshots, mockups, Figma files
│
├── Web Search
│   └── Real-time documentation and API references
│
└── Rules & Guidelines
    └── Team coding standards enforcement
```

---

## CONTEXT ENGINE

### 3. What the Context Engine Tracks

```
Context Engine (Live)
│
├── Code structure and dependencies
│   └── Real-time indexing of files, symbols, graphs
│
├── Architecture patterns
│   └── Conventions and design shape
│
├── Project history
│   └── Commit history and recent changes
│
├── Documentation & style
│   └── READMEs, style guides, code comments
│
└── Issues & technical debt
    └── Known hotspots and TODOs
```

---

### 4. Precision Example

```
Context Engine — Filtering
│
├── Raw sources       4,456
├── Relevant sources    682
└── Precision boost   ~6.5× signal density
```

---

## PRODUCTS

### 5. Product Surfaces

```
Augment Code — Products
│
├── IDE Agent
│   ├── VS Code
│   └── JetBrains (IntelliJ, WebStorm, PyCharm, GoLand, Rider, PhpStorm, RubyMine, CLion)
│
├── CLI
│   └── Terminal agent using the same Context Engine
│
├── Intent
│   └── Coordinated multi-agent workspace
│
├── Code Review
│   └── AI reviewer with inline GitHub comments
│
├── Slack
│   └── Team collaboration (Enterprise)
│
└── Context Engine MCP
    └── Expose codebase context to other agents
```

---

## INTEGRATIONS

### 6. Native & MCP Integrations

```
Integrations
│
├── Native
│   ├── GitHub
│   ├── Linear
│   ├── Jira
│   ├── Confluence
│   ├── Notion
│   ├── Sentry
│   └── Stripe
│
└── MCP
    ├── Figma
    ├── Stripe
    ├── MongoDB
    ├── AWS
    └── 100+ community tools
```

---

## BENCHMARKS

### 7. Performance Claims

```
Performance
│
├── SWE-Bench Pro
│   └── Top of leaderboard at 51.80% (vs. 46–50% competitors)
│
└── Elasticsearch blind study (3.6M Java LOC)
    ├── Correctness   +12.8% vs. humans
    ├── Completeness  +18.2% vs. humans
    └── Code reuse    +14.8% vs. humans
```

---

## PRICING

### 8. Plans

```
Pricing Tiers
│
├── Indie — $20 / month
│   ├── 40,000 credits
│   ├── Up to 1 user
│   └── Context Engine, Agent, Intent, Chat, MCP, Code Review
│
├── Standard — $60 / developer / month  (Most Popular)
│   ├── 130,000 credits
│   ├── Up to 20 users
│   └── + Advanced Analytics, GitHub Multi-Org
│
├── Max — $200 / developer / month
│   ├── 450,000 credits
│   ├── Up to 20 users
│   └── All Standard features, for heavy usage
│
└── Enterprise — Custom
    ├── Custom credits and top-ups
    ├── Unlimited users
    └── + Slack, SSO/OIDC/SCIM, CMEK, ISO 42001, dedicated support
```

---

## TRUST & COMPLIANCE

### 9. Security Posture

```
Trust & Compliance
│
├── SOC 2 Type II                 (all tiers)
├── No training on user data      (all tiers)
├── SSO / OIDC / SCIM             (Enterprise)
├── CMEK                          (Enterprise)
├── ISO 42001                     (Enterprise)
├── Trust Center & Privacy docs
├── SLA and Support Policy
└── Public status page
```

---

## Augment Code — Big Picture

```
Augment Code — Big Picture
│
├── 1. PLAN
│   ├── Context-aware planning
│   │   ├── Breaks requests into actionable steps
│   │   ├── Grounded in real codebase structure
│   │   └── Auto-expands prompts with relevant context
│   └── Ask Mode
│       └── Read-only exploration without edits
│
├── 2. IMPLEMENT
│   ├── IDE Agent
│   │   ├── VS Code
│   │   └── JetBrains (IntelliJ, PyCharm, WebStorm, GoLand, Rider, PhpStorm, RubyMine, CLion)
│   ├── CLI Agent
│   │   └── Terminal agent on the same Context Engine
│   ├── Agent Capabilities
│   │   ├── Auto Mode               → plan + implement end-to-end
│   │   ├── Parallel Tool Calls     → simultaneous operations
│   │   ├── Terminal Execution      → npm, git, tests
│   │   ├── Image Understanding     → screenshots, Figma, mockups
│   │   ├── Web Search              → live docs and APIs
│   │   └── Multi-Model             → Claude, GPT, frontier models
│   └── Intent (Workspace)
│       ├── Living specification
│       ├── Coordinated multi-agent team
│       ├── Isolated dev environments
│       └── Parallel task breakdown
│
├── 3. REVIEW
│   ├── Checkpoints
│   │   └── Snapshot and rollback
│   ├── AI Code Review
│   │   ├── Inline GitHub comments
│   │   ├── Full codebase context
│   │   └── One-click IDE fixes
│   └── Memory Review
│       └── Approve or edit agent memories before storage
│
├── 4. INTEGRATE
│   ├── Native
│   │   ├── GitHub, Linear, Jira
│   │   ├── Confluence, Notion
│   │   └── Sentry, Stripe
│   ├── MCP
│   │   ├── Figma, Stripe, MongoDB, AWS
│   │   └── 100+ community tools
│   ├── Slack                    (Enterprise)
│   ├── Context Engine MCP       (expose context to other agents)
│   └── Rules & Guidelines       (team coding standards)
│
├── 5. SCALE
│   ├── SOC 2 Type II
│   ├── No training on user data
│   ├── SSO / OIDC / SCIM         (Enterprise)
│   ├── CMEK & ISO 42001          (Enterprise)
│   ├── Multi-Repo Support
│   └── Enterprise monorepos      (e.g., 3.6M+ LOC)
│
├── 6. CONTEXT ENGINE
│   ├── Code structure & dependencies
│   ├── Architecture patterns
│   ├── Project history & commits
│   ├── Docs & style conventions
│   └── Issues & technical debt
│
├── 7. BENCHMARKS
│   ├── SWE-Bench Pro — 51.80% (top)
│   └── Elasticsearch blind study
│       ├── Correctness   +12.8%
│       ├── Completeness  +18.2%
│       └── Code reuse    +14.8%
│
└── 8. PRICING
    ├── Indie        $20 / mo     — 40K credits, 1 user
    ├── Standard     $60 / dev    — 130K credits, up to 20 users
    ├── Max          $200 / dev   — 450K credits, up to 20 users
    └── Enterprise   Custom       — unlimited users, SSO/CMEK/ISO 42001
```
