<div align="center">

<img src="https://img.shields.io/badge/Terraform-Mission_Control-7c3aed?style=for-the-badge&logo=terraform&logoColor=white" alt="Terraform Mission Control"/>

# 🚀 terraform-labs

**A fully gamified, interactive Terraform learning platform.**
Complete quests, earn XP, flip flashcards, copy snippets, and level up from Beginner to Platform Engineer.

[![Live Demo](https://img.shields.io/badge/🌐_Live-terraform.eknathalabs.com-00e5ff?style=for-the-badge)](https://terraform.eknathalabs.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-7c3aed?style=for-the-badge)](LICENSE)
[![Made by EknathaLabs](https://img.shields.io/badge/By-EknathaLabs-10b981?style=for-the-badge)](https://eknathalabs.com)
[![GitHub](https://img.shields.io/badge/GitHub-eknatha-f59e0b?style=for-the-badge&logo=github)](https://github.com/eknatha)

<br/>

> Built for DevOps engineers and Platform Engineering aspirants who learn by **doing**, not just watching.

</div>

---

## 📸 What Is This?

`terraform-labs` is a **single-file, offline-capable gamified web app** that turns Terraform learning into a real game — with XP, levels, quests, timed simulations, flashcard drills, a snippet library, leaderboard, and achievement badges.

No backend. No login. No subscription. Everything runs in the browser and persists in `localStorage`.

**Open [`terraform.eknathalabs.com`](https://terraform.eknathalabs.com) and start earning XP.**

---

## ✨ Features

### 🎮 Core Game Engine
| Feature | Description |
|---|---|
| **XP & Level System** | Earn XP for every action — objectives, quizzes, drills, simulations, daily challenges. 8 levels from `ROOKIE` → `PRINCIPAL` |
| **Operator Profile** | Enter your callsign on first launch. Personalises the HUD, hero greeting, and dashboard |
| **Day Streak Tracker** | Claim the daily challenge every day to build your streak |
| **Confetti Celebrations** | Canvas-based particle burst fires on every quest completion |
| **Dark / Light Mode** | Toggle between terminal-dark and clean-light themes. Preference saved across sessions |
| **Live XP in Tab Title** | Browser tab shows your current XP so you can track progress while switching tabs |

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
- 💡 **Solution guides** — every objective has a `▼ SOLUTION` toggle with a full explanation, syntax-highlighted HCL/YAML code, and a pro tip
- 🧠 **Knowledge quiz** — a multiple-choice question that must be passed to complete the quest
- 🔒 **Locked progression** — quests unlock sequentially, no skipping

### 🃏 Flashcard Drill Mode
- **60 cards** across 5 categories: Basics, State, Modules, CI/CD, Security
- **3D flip animation** — click to flip from question to answer
- **Spaced repetition** — cards marked "Review Again" reappear 2× more often
- **Category filters** — drill only State cards, or only Security cards
- **Session summary** — Got It / Review count, XP earned, accuracy %
- **Review queue** — all missed cards in one filtered view

### 📋 HCL Snippet Library
- **62 production-ready snippets** across AWS, GCP, Azure, and multi-cloud patterns
- **Live search** — filters across title, description, code, provider, and type simultaneously
- **10 filter buttons** — ALL / AWS / GCP / AZURE / STATE / NETWORKING / COMPUTE / IAM / CI/CD / SECURITY
- **Syntax highlighting** — keywords, strings, keys, comments colour-coded
- **One-click copy** — copies raw HCL to clipboard and earns +2 XP

**Snippet categories include:**
- S3/GCS/Azure remote backends
- AWS VPC, subnets, NAT Gateway, security groups
- EC2, Launch Templates, Auto Scaling Groups
- IAM roles, OIDC trust policies, instance profiles
- GitHub Actions plan-on-PR and apply-on-merge workflows
- Module structure patterns (`variables.tf`, `outputs.tf`, `locals`, `dynamic`, `for_each`)
- GCP VPC, GKE autopilot cluster, Cloud SQL, service accounts
- Azure VNet, AKS cluster, resource groups
- Security patterns: `prevent_destroy`, `sensitive`, `precondition`, variable validation
- Advanced: `moved` block, `check` block, `import` block, multi-region aliases, provider aliases

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

### 🏅 Achievement Badges
10 badges that auto-unlock when you hit milestones:

`🟢 FIRST APPLY` `🔐 STATE GUARDIAN` `📦 MODULE BUILDER` `⚡ PIPELINE RUNNER` `🚨 DRIFT BUSTER` `🏆 PLATFORM ENGINEER` `🏎️ SPEED RUNNER` `🌍 MULTI-CLOUD OPS` `⭐ DAILY WARRIOR` `💯 XP CENTURION`

### 🏆 Leaderboard
Live rank against 7 simulated competitors. Your real XP is inserted and re-sorted dynamically.

### 📊 Dashboard
- Operator profile card with initials avatar, level, join date
- Live stats: Total XP, Quests Done, Objectives, Badges, Simulations, Streak
- Full activity log with timestamps

### 💡 Did You Know? Tip Bar
20 rotating production Terraform tips displayed in a persistent bar below the HUD. Auto-rotates every 8 seconds. Manual navigation with `‹` / `›` buttons.

### 📅 Daily Challenge
5 rotating challenges (resets at midnight). Claim each day to earn bonus XP and maintain your streak.

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

> The entire application — all game logic, 62 snippets, 60 flashcards, 6 quests with solutions, simulations, and themes — is contained in a **single `index.html` file** with no external dependencies beyond Google Fonts.

---

## 🚀 Quick Start

### Option 1 — Use the live site
Open **[terraform.eknathalabs.com](https://terraform.eknathalabs.com)** in your browser. That's it.

### Option 2 — Run locally
```bash
git clone https://github.com/eknatha/terraform-labs.git
cd terraform-labs

# No build step needed — just open the file:
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Or serve with any static server:
python3 -m http.server 8080
# then open http://localhost:8080
```

### Option 3 — Host on GitHub Pages
```bash
# Already set up at terraform.eknathalabs.com
# To fork and host your own:
# 1. Fork this repo
# 2. Go to Settings → Pages
# 3. Source: Deploy from branch → main → / (root)
# 4. Add your custom domain (optional)
```

---

## 🎯 Who Is This For?

| Person | How to use it |
|---|---|
| **DevOps engineer learning Terraform** | Work through Quests 1–3 in order. Use the Snippets tab during KodeKloud labs |
| **Platform Engineering aspirant** | Complete all 6 quests. Focus on Quest 4–6 for production-grade patterns |
| **Preparing for Terraform Associate cert** | Use Flashcard Drill Mode daily. Filter by each exam domain category |
| **Preparing for a PE interview** | Quest 5 & 6 solutions map directly to "describe a production incident" questions |
| **Senior engineer onboarding a team** | Share the URL — it's a free, no-login training resource for your team |

---

## 📐 Tech Stack

| Layer | Technology |
|---|---|
| **Framework** | Vanilla HTML + CSS + JavaScript — zero dependencies |
| **Fonts** | Orbitron, Share Tech Mono, Rajdhani (Google Fonts) |
| **Storage** | Browser `localStorage` — all progress persists client-side |
| **Confetti** | Custom canvas particle engine (no library) |
| **Syntax highlighting** | Regex-based HCL tokeniser (no library) |
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

- [ ] Interview simulation mode (AI-scored PE interview questions)
- [ ] GCP learning track (4 dedicated quests)
- [ ] Study calendar heatmap (GitHub-style activity grid)
- [ ] Shareable progress card (PNG download for LinkedIn)
- [ ] Mock Terraform Associate exam (57Q / 60 min)
- [ ] Terraform Plan Explainer (paste plan output → plain English)
- [ ] Pomodoro focus timer in HUD
- [ ] LinkedIn post generator (auto-trigger on milestones)
- [ ] Community snippet submissions (GitHub Issue → PR flow)

---

## 🤝 Contributing

Contributions are welcome — especially new HCL snippets, flashcard questions, and quest objectives.

### Submit a Snippet
1. Open an [Issue](https://github.com/eknatha/terraform-labs/issues/new) using the **Snippet Submission** template
2. Provide: title, provider (aws/gcp/azure/multi), type, HCL code, one-line description
3. I'll review and merge into the Snippets tab

### Submit a Flashcard
Open an Issue with the **Flashcard** label:
- Front: the question
- Back: the answer (ideally with a code example)
- Category: basics / state / modules / cicd / security

### General PRs
```bash
# Fork → clone → branch → commit → PR
git checkout -b feat/your-feature
git commit -m "feat: add [description]"
git push origin feat/your-feature
# Open PR against main
```

Commit message convention: `feat:` / `fix:` / `docs:` / `chore:` — keeps the git log clean.

---

## 📄 License

MIT © [EknathaLabs](https://eknathalabs.com) · [@eknatha](https://github.com/eknatha)

Free to use, fork, and build on. If this helped you — a ⭐ star goes a long way.

---

<div align="center">

**Built with 🔥 by [EknathaLabs](https://eknathalabs.com)**

[Live App](https://terraform.eknathalabs.com) · [GitHub](https://github.com/eknatha) · [Issues](https://github.com/eknatha/terraform-labs/issues)

</div>
