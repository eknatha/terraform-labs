<div align="center">

<img src="https://img.shields.io/badge/Terraform-Mission_Control-7c3aed?style=for-the-badge&logo=terraform&logoColor=white" alt="Terraform Mission Control"/>

# 🚀 terraform-labs

**A fully gamified, interactive Terraform learning platform.**
Complete quests, earn XP, study architecture patterns, flip flashcards, copy snippets, and level up from Beginner to Platform Engineer.

[![Live Demo](https://img.shields.io/badge/🌐_Live-terraform.eknathalabs.com-00e5ff?style=for-the-badge)](https://terraform.eknathalabs.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-7c3aed?style=for-the-badge)](LICENSE)
[![Made by EknathaLabs](https://img.shields.io/badge/By-EknathaLabs-10b981?style=for-the-badge)](https://eknathalabs.com)
[![GitHub](https://img.shields.io/badge/GitHub-eknatha-f59e0b?style=for-the-badge&logo=github)](https://github.com/eknatha)

<br/>

> Built for DevOps engineers and Platform Engineering aspirants who learn by **doing**, not just watching.

</div>

---

## 📸 What Is This?

`terraform-labs` is a **single-file, offline-capable gamified web app** that turns Terraform learning into a real game — with XP, levels, quests, timed simulations, flashcard drills, a snippet library, daily micro-learning features, an architecture pattern library, interactive concept map, quiz mode, leaderboard, and achievement badges.

No backend. No login. No subscription. Everything runs in the browser and persists in `localStorage`.

**Open [`terraform.eknathalabs.com`](https://terraform.eknathalabs.com) and start earning XP.**

---

## ✨ Features

### 🎮 Core Game Engine

| Feature | Description |
|---|---|
| **XP & Level System** | Earn XP for every action — objectives, quizzes, drills, simulations, daily features. 8 levels from `ROOKIE` → `PRINCIPAL` |
| **Operator Profile** | Enter your callsign on first launch — personalises the HUD, hero greeting, and dashboard |
| **Day Streak Tracker** | Claim the daily challenge every day to build your streak |
| **Confetti Celebrations** | Canvas-based particle burst fires on every quest completion |
| **Dark / Light Mode** | Toggle between terminal-dark and clean-light themes — preference saved across sessions |
| **Live XP in Tab Title** | Browser tab shows your current XP so you can track progress while switching tabs |
| **Live Visitor Counter** | Real-time global visitor count in the footer and dashboard (counterapi.dev, session-deduplicated) |

---

### ⚔️ Quest System (6 Quests)

| Quest | Level | Topic | XP |
|---|---|---|---|
| Quest 1 — Origin Story | 🟢 Beginner | First `main.tf`, init/plan/apply cycle, local provider | +250 |
| Quest 2 — State of the Nation | 🟢 Beginner | `tfstate`, S3 remote backend, DynamoDB locking, drift detection | +400 |
| Quest 3 — Module Architect | 🔵 Intermediate | Reusable modules, `for_each`, `locals`, `outputs.tf` | +600 |
| Quest 4 — Pipeline Commander | 🔵 Intermediate | GitHub Actions CI/CD, OIDC auth, plan on PR, checkov | +800 |
| Quest 5 — Drift Detector | 🟣 Advanced | Drift detection, `terraform import`, scheduled alerts, postmortem | +1000 |
| Quest 6 — Boss Fight | 🔴 Expert | Multi-account landing zone, Atlantis, OPA policies, cross-account IAM | +1500 |

**Each quest includes:**
- ✅ **Interactive objectives** — click to complete and earn XP
- 💡 **Solution guides** — every objective has a `▼ SOLUTION` toggle with explanation, syntax-highlighted HCL/YAML, and a pro tip
- 🧠 **Knowledge quiz** — a multiple-choice question that must be passed to complete the quest
- 🔒 **Locked progression** — quests unlock sequentially, no skipping

---

### 🃏 Flashcard Drill Mode

- **60 cards** across 5 categories: Basics, State, Modules, CI/CD, Security
- **3D flip animation** — click to flip from question to answer
- **Spaced repetition** — cards marked "Review Again" reappear 2× more often
- **Category filters** — drill only State cards, or only Security cards
- **Session summary** — Got It / Review count, XP earned, accuracy %
- **Review queue** — all missed cards in one filtered view

---

### 📋 HCL Snippet Library

- **62 production-ready snippets** across AWS, GCP, Azure, and multi-cloud patterns
- **Live search** — filters across title, description, code, provider, and type simultaneously
- **10 filter buttons** — ALL / AWS / GCP / AZURE / STATE / NETWORKING / COMPUTE / IAM / CI/CD / SECURITY
- **Syntax highlighting** — keywords, strings, keys, comments colour-coded
- **One-click copy** — copies raw HCL to clipboard and earns +2 XP

Snippet categories: S3/GCS/Azure backends · AWS VPC/subnets/NAT/security groups · EC2/Launch Templates/ASG · IAM roles/OIDC · GitHub Actions workflows · Module patterns (`variables.tf`, `outputs.tf`, `locals`, `dynamic`, `for_each`) · GCP VPC/GKE/Cloud SQL · Azure VNet/AKS · `moved`, `check`, `import` blocks · multi-region provider aliases

---

### ⚡ Timed Simulations

6 scenario-based drills with real countdown timers:

| Simulation | Difficulty | Time | XP |
|---|---|---|---|
| Break & Fix: State Corruption | Intermediate | 15 min | +150 |
| Speed Run: VPC Deploy | Beginner | 30 min | +100 |
| Plan Output Literacy | Beginner | 10 min | +80 |
| Incident Roleplay | Advanced | 20 min | +200 |
| Multi-Cloud Parity Build | Advanced | 40 min | +250 |
| Terratest Gauntlet | Expert | 60 min | +300 |

---

## 📅 Daily Micro-Learning — 7 Daily Features

Build a 15-minute daily study habit. Fresh content rotates every day across all seven features.

| Tab | What you get | XP | Resets |
|---|---|---|---|
| ⌨️ **CMD** | Command of the Day — syntax, all flags, 2 examples with COPY, when NOT to use | +5 | Daily |
| 📐 **ARCH** | Architecture Pattern — ASCII diagram, Terraform sketch, trade-offs, pro tip | +10 | Daily |
| 🔤 **TERM** | Term of the Day — pronunciation, definition, analogy, why it matters, code | +3 | Daily |
| ⚠️ **ERROR** | Error of the Day — exact error text, root cause, numbered fix steps, prevention | +5 | Daily |
| 🎤 **DAILY IQ** | Interview Question — full answer, working code example, pro tip | +40–70 | Daily |
| ❓ **QUIZ** | Multiple-choice question mapped to Terraform Associate exam domains | +4 correct / +1 try | Daily |
| 📅 **Daily Challenge** | Hands-on challenge with full answer, numbered steps, HCL example | Varies | Daily |

### ⌨️ Command of the Day — 40 commands

Rotating daily across Basics · State · Modules · CI/CD · Debug. Every card shows: syntax, all flags with descriptions, 2 real-world examples with COPY buttons, a "When NOT to use" warning, and a pro tip. Previous 18 commands shown in an expandable history grid.

### 📐 Architecture Pattern of the Day — 30 patterns

One production architecture pattern every day. Every card shows an ASCII topology diagram, Terraform code sketch with COPY button, side-by-side pros/cons trade-off panel, and a pro tip. Previous 18 patterns in expandable history grid.

**Pattern categories:** Networking · Compute · Security · CI/CD · Storage · Kubernetes · Resilience · Multi-cloud

**Sample patterns:** Hub-and-Spoke VPC · Zero-Trust with PrivateLink · Multi-AZ Active-Active · Blue-Green with ALB Weighted Routing · S3 Multi-Region Replication · GKE Private Cluster + Cloud SQL Proxy · GitOps with ArgoCD on EKS · VPC Endpoint Gateway · IAM Permission Boundaries · Direct Connect + VPN Backup · Spot Instance Fleet · Multi-Region Active-Passive + Route 53 · EKS IRSA · AWS WAF + ALB · Multi-Cloud Active-Active · Terraform GitOps with Atlantis · Secrets Manager · VPC Flow Logs → Athena · ECS Fargate + Service Connect · SQS Dead Letter Queue · S3 Event Pipeline · Terraform Multi-Account Landing Zone · EKS Karpenter · DNS Service Discovery · and 6 more

### 🔤 Term of the Day — 50 terms

Across Terraform · DevOps · Kubernetes · CI/CD · Security. Each term: phonetic pronunciation, plain-English definition, a real-world analogy, why it matters in production, and a code example.

**Sample terms:** Idempotency · Drift · State · Backend · Provider · Module · GitOps · Immutable Infrastructure · SLA/SLO/SLI · Blast Radius · MTTR · Observability · Zero Downtime Deployment · Least Privilege · OIDC · for\_each · Lifecycle · Dynamic Block · Golden Path · Sensitive Value · Technical Debt · Toil · Shift Left · Canary Release · mTLS · On-Call · and 25 more

### ⚠️ Error of the Day — 30 real errors

Across STATE · AUTH · CONFIG · PLAN · BACKEND · IAM · PROVIDER. Every error card: exact terminal error text, root cause, numbered fix steps, exact commands with COPY button, and how to prevent recurrence. Severity: HIGH (red) · MED (amber).

**Sample errors:** Error acquiring state lock · No valid credentials · Missing required argument · Resource not found in state · Corrupted state file · Unsupported argument (provider upgrade) · Reference to undeclared resource · Circular dependency cycle · Backend config changed · Provider inconsistent result · Validation failed · AccessDenied 403 · Corrupted JSON state · Assume role failed · Resource already exists · Invalid for\_each argument · Provider version mismatch · and 13 more

### 🎤 Interview Question of the Day — 60 questions

Across Terraform · Kubernetes · Linux · CI/CD · AWS · GCP. Full answers, working code examples with COPY, and pro tips. Previous 18 questions in an expandable history grid showing full answers inline.

### ❓ Quiz of the Day — 100 questions

Mapped to the 6 official Terraform Associate exam domains. Instant feedback — correct turns green, wrong turns red, correct answer always revealed. Explanation shown after every answer. Separate **Quiz Streak** tracks consecutive correct days. Live stats: Quiz Streak · Correct · Total · Accuracy %.

| Exam Domain | Weight |
|---|---|
| Terraform Basics | 36% |
| Terraform Modules | 22% |
| Terraform Cloud / HCP | 16% |
| IaC Concepts | 14% |
| Terraform Purpose | 8% |
| Terraform Workflow | 4% |

---

## 🗺️ Terraform Concept Map

Interactive SVG diagram showing all core Terraform concepts and their relationships — rendered in-browser, no external libraries.

**10 clickable nodes:** Provider · Resource · Variable · Output · Module · State · Locals · Backend · Plan/Apply · Workspace

Click any node → see its definition, why it matters in production, a code example, and a **▶ OPEN QUEST** button that jumps directly to the relevant quest. Animated dashed dependency edges show relationship labels (creates · tracked in · stored in · inputs to · isolates · etc.).

---

### 🏅 Achievement Badges

10 badges that auto-unlock when you hit milestones:

`🟢 FIRST APPLY` `🔐 STATE GUARDIAN` `📦 MODULE BUILDER` `⚡ PIPELINE RUNNER` `🚨 DRIFT BUSTER` `🏆 PLATFORM ENGINEER` `🏎️ SPEED RUNNER` `🌍 MULTI-CLOUD OPS` `⭐ DAILY WARRIOR` `💯 XP CENTURION`

### 🏆 Leaderboard
Live rank against 7 simulated competitors. Your real XP is inserted and re-sorted dynamically.

### 📊 Dashboard
- Operator profile card with initials avatar, level, and join date
- Live stats: Total XP · Quests Done · Objectives · Badges · Simulations · Streak
- Global visitor counter — live total visits to terraform.eknathalabs.com
- Full activity log with timestamps

### 💡 Did You Know? Tip Bar
20 rotating production Terraform tips in a persistent bar below the HUD. Auto-rotates every 8 seconds. Manual `‹` / `›` navigation.

---

## 📊 Content at a Glance

| Content Type | Count |
|---|---|
| Quests with full solution guides | 6 |
| Quest objectives with ▼ SOLUTION toggles | 30 |
| Flashcards (5 categories) | 60 |
| HCL snippets (AWS / GCP / Azure / multi-cloud) | 62 |
| Timed simulations | 6 |
| Achievement badges | 10 |
| Concept map nodes | 10 |
| Architecture patterns (ARCH tab) | 30 |
| Commands of the day (CMD tab) | 40 |
| Terms of the day (TERM tab) | 50 |
| Real Terraform errors (ERROR tab) | 30 |
| Interview questions (DAILY IQ tab) | 60 |
| Quiz questions — exam-mapped (QUIZ tab) | 100 |
| Daily challenges with full answers | 5 |

---

## 🗂️ Repository Structure

```
terraform-labs/
├── index.html              ← Entire app — single file, no dependencies
├── README.md               ← This file
├── LICENSE                 ← MIT
└── .github/
    └── ISSUE_TEMPLATE/
        └── snippet-submission.md
```

> The entire application — 10+ learning tabs, 100 quiz questions, 30 architecture patterns, 50 terms, 30 errors, 40 commands, 60 interview questions, 62 snippets, 60 flashcards, 6 quests with solutions, simulations, concept map, and dual themes — is a **single `index.html` file** with zero external dependencies beyond Google Fonts.

---

## 🚀 Quick Start

### Option 1 — Use the live site
Open **[terraform.eknathalabs.com](https://terraform.eknathalabs.com)** in your browser. That's it.

### Option 2 — Run locally
```bash
git clone https://github.com/eknatha/terraform-labs.git
cd terraform-labs

# No build step — just open the file:
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Or serve with any static server:
python3 -m http.server 8080
# then open http://localhost:8080
```

### Option 3 — Host on GitHub Pages
```bash
# Already live at terraform.eknathalabs.com
# To fork and host your own:
# 1. Fork this repo
# 2. Settings → Pages → Deploy from branch → main → / (root)
# 3. Add your custom domain (optional)
```

---

## 🎯 Who Is This For?

| Person | How to use it |
|---|---|
| **DevOps engineer learning Terraform** | Work through Quests 1–3 in order. Use Snippets and CMD tab during KodeKloud labs |
| **Platform Engineering aspirant** | Complete all 6 quests. Use ARCH tab daily for architecture interview preparation |
| **Preparing for Terraform Associate cert** | Use QUIZ tab daily — 100 questions across all 6 official exam domains |
| **Preparing for a PE interview** | ARCH patterns + DAILY IQ map directly to "describe a production design" questions |
| **Building a daily study habit** | CMD + TERM + ERROR + QUIZ = 15-minute daily ritual |
| **Senior engineer onboarding a team** | Share the URL — free, no-login, production-grade reference for the whole team |

---

## 📐 Tech Stack

| Layer | Technology |
|---|---|
| **Framework** | Vanilla HTML + CSS + JavaScript — zero dependencies |
| **Fonts** | Orbitron, Share Tech Mono, Rajdhani (Google Fonts) |
| **Storage** | Browser `localStorage` — all progress persists client-side |
| **Confetti** | Custom canvas particle engine (no library) |
| **Syntax highlighting** | Regex-based HCL tokeniser (no library) |
| **Concept map** | SVG rendered in-browser with animated edges (no library) |
| **Visitor counter** | counterapi.dev free tier — session-deduplicated daily counts |
| **Themes** | CSS custom properties with `body.light-mode` toggle |
| **Hosting** | GitHub Pages with custom domain |

---

## 🗺️ Learning Path

```
🟢 Tier 1 — Fundamentals     init · plan · apply · providers · variables
🔵 Tier 2 — State Mastery    remote backends · locking · state mv/rm · import
🔵 Tier 3 — Modules & Reuse  module structure · locals · outputs · registry
🌍 Tier 4 — Workspaces       workspaces · tfvars · for_each · count
⚡ Tier 5 — CI/CD             GitHub Actions · Atlantis · OIDC auth · plan on PR
🛡️ Tier 6 — Policy & Security Sentinel · OPA/conftest · checkov · tfsec
🔴 Tier 7 — Production        landing zones · multi-account · Terragrunt · drift
```

Skill tiers unlock automatically as you complete quests. Each tier maps to real Platform Engineer interview questions.

---

## 🏗️ Roadmap

- [ ] Study heatmap — GitHub-style 12-week XP activity grid in the dashboard
- [ ] Progress card download — PNG card (name, level, XP, badges) for LinkedIn / GitHub README
- [ ] Cert readiness gauge — live % toward Terraform Associate pass mark, green at 70%
- [ ] Mock exam — 57Q / 60 min, per-domain scoring, "Book the exam" CTA
- [ ] AI interview coach — Claude grades your IQ answers with strengths, gaps, and ideal answer
- [ ] LinkedIn post generator — pre-written post auto-triggered after quest/badge/level milestones
- [ ] Pomodoro focus timer — 25-min HUD timer, +30 XP per completed session
- [ ] XP combo multiplier — complete CMD + Challenge + IQ in one day = 1.5× XP until midnight
- [ ] Streak freeze token — earn 1 freeze every 7 streak days, auto-protects on a missed day
- [ ] GCP learning track — 4 dedicated quests: GKE, Cloud SQL, VPC, Workload Identity
- [ ] 30-day Terraform challenge — one task per day, pledge card on day 1, certificate on day 30
- [ ] Hall of Fame — list of engineers who completed all 6 quests (submit via GitHub Issue)
- [ ] Community snippet submissions — GitHub Issue → PR flow with contributors section

---

## 🤝 Contributing

Contributions are welcome — especially new HCL snippets, flashcard questions, architecture patterns, and quiz questions.

### Submit a Snippet
1. Open an [Issue](https://github.com/eknatha/terraform-labs/issues/new) using the **Snippet Submission** template
2. Provide: title, provider (aws/gcp/azure/multi), type, HCL code, one-line description
3. Reviewed and merged into the Snippets tab

### Submit a Quiz Question
Open an Issue with the **Quiz Question** label and include:
- Question text
- 4 answer options with the correct one indicated
- Exam domain: Terraform Basics / Modules / Cloud / IaC Concepts / Purpose / Workflow
- One-sentence explanation of why the correct answer is right

### Submit a Flashcard
Open an Issue with the **Flashcard** label:
- Front: the question
- Back: the answer (with a code example where possible)
- Category: basics / state / modules / cicd / security

### General PRs
```bash
# Fork → clone → branch → commit → PR
git checkout -b feat/your-feature
git commit -m "feat: add [description]"
git push origin feat/your-feature
# Open PR against main
```

Commit message convention: `feat:` / `fix:` / `docs:` / `chore:`

---

## 📄 License

MIT © [EknathaLabs](https://eknathalabs.com) · [@eknatha](https://github.com/eknatha)

Free to use, fork, and build on. If this helped you — a ⭐ star goes a long way.

---

<div align="center">

**Built with 🔥 by [EknathaLabs](https://eknathalabs.com)**

[Live App](https://terraform.eknathalabs.com) · [GitHub](https://github.com/eknatha) · [Issues](https://github.com/eknatha/terraform-labs/issues)

</div>
