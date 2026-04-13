# 🚀 terraform-labs

> **Gamified Terraform learning** — quests, simulations, modules, and production-grade IaC patterns.  
> Built for DevOps & Platform Engineers who learn by doing.

[![Live Guide](https://img.shields.io/badge/🌐_Live_Guide-terraform.eknathalabs.com-00e5ff?style=for-the-badge)](https://terraform.eknathalabs.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-7c3aed?style=for-the-badge)](LICENSE)
[![Level](https://img.shields.io/badge/Level-Beginner_→_Expert-10b981?style=for-the-badge)](#learning-path)
[![By EknathaLabs](https://img.shields.io/badge/By-EknathaLabs-f59e0b?style=for-the-badge)](https://eknathalabs.com)

---

## 🎯 What Is This?

`terraform-labs` is a **quest-based, gamified learning repository** for mastering Terraform (Infrastructure as Code).  
Instead of passive reading, you earn XP, complete timed challenges, simulate production failures, and build a real portfolio of IaC projects — all structured as a game.

**Who is this for?**
- L2/L3 engineers transitioning into Platform Engineering
- DevOps engineers preparing for the **Terraform Associate** certification
- Anyone who learns better by *building* than by watching

---

## 🗺️ Learning Path — 6 Quests

| Quest | Level | Topic | XP | Tools |
|-------|-------|-------|----|-------|
| 01 | 🟢 Beginner | Terraform Origin Story — first `main.tf`, providers, resources | +250 | `local` provider |
| 02 | 🟢 Beginner | State of the Nation — tfstate, remote backends, locking | +400 | S3 + DynamoDB |
| 03 | 🔵 Intermediate | Module Architect — reusable modules, inputs/outputs, workspaces | +600 | AWS / Azure |
| 04 | 🔵 Intermediate | Pipeline Commander — GitHub Actions CI/CD, plan on PR, apply on merge | +800 | GitHub Actions |
| 05 | 🟣 Advanced | Drift Detector — detect & fix infrastructure drift, import, taint | +1000 | Multi-cloud |
| 06 | 🔴 Expert | Platform Engineer Boss Fight — multi-account landing zone, Atlantis, GitOps | +1500 | Atlantis + TFE |

> **Total: 4,550 XP** — complete all 6 quests to unlock the `TERRAFORM PLATFORM ENGINEER` badge.

---

## 📂 Repository Structure

```
terraform-labs/
├── quests/
│   ├── quest-01-origin-story/
│   ├── quest-02-state-management/
│   ├── quest-03-module-architect/
│   ├── quest-04-pipeline-commander/
│   ├── quest-05-drift-detector/
│   └── quest-06-boss-fight/
├── modules/
│   ├── vpc/
│   └── compute/
├── simulations/
│   ├── break-and-fix/
│   └── drift-detection/
├── docs/
│   └── index.html          ← Live guide at terraform.eknathalabs.com
└── .github/
    └── workflows/
```

---

## ⚡ Quick Start — Quest 1 (No Cloud Account Needed)

```bash
# Clone the repo
git clone https://github.com/eknatha/terraform-labs.git
cd terraform-labs/quests/quest-01-origin-story

# Initialize and deploy your first resource
terraform init
terraform plan
terraform apply

# Inspect what was created
cat mission_log.txt
cat terraform.tfstate

# Clean up
terraform destroy
```

> **Goal:** Understand the init → plan → apply → destroy cycle before touching any cloud provider.

---

## 🧪 Simulation Techniques

| Technique | What You Practice |
|-----------|-------------------|
| 💥 **Break-and-Fix Drills** | Corrupt `.tfstate`, recover using `import` / `state rm` |
| 🏎️ **Speed-Run Challenges** | Deploy a 3-tier VPC in under 30 minutes — track your time weekly |
| 🌍 **Multi-Cloud Parity Builds** | Same architecture on AWS + GCP using identical module interfaces |
| 🔍 **Plan Output Reading** | Predict what `apply` will do before running it — score yourself |
| 🚨 **Incident Roleplay** | Simulate accidental `terraform destroy` and full recovery |
| 🧪 **Terratest Automation** | Write Go-based assertions that validate infra actually works |

---

## 🛠️ Platforms Used in This Repo

| Platform | Cost | Best For |
|----------|------|----------|
| [KodeKloud](https://kodekloud.com) | Paid | Browser-based labs with real cloud sandboxes |
| [HashiCorp Learn](https://developer.hashicorp.com/terraform/tutorials) | Free | Official guided tutorials with in-browser terminal |
| [Instruqt](https://instruqt.com) | Freemium | Game-like track system, HashiCorp partner labs |
| [LocalStack](https://localstack.cloud) | Free | Local AWS emulator — zero cost, zero cloud account |
| [Pluralsight / ACG](https://acloudguru.com) | Paid | Skill IQ scoring + cloud sandboxes |

---

## 🧠 Terraform Skill Tree

```
🟢 Tier 1 — Fundamentals        init / plan / apply / providers / variables
🔵 Tier 2 — State Mastery        remote backends / locking / state mv / import
🔵 Tier 3 — Modules & Reuse      module structure / locals / outputs / registry
🟣 Tier 4 — Workspaces & Envs    workspaces / tfvars / loops / for_each
🟣 Tier 5 — CI/CD Integration    GitHub Actions / Atlantis / OIDC auth
🟡 Tier 6 — Policy & Security    Sentinel / OPA / conftest / checkov / tfsec
🔴 Tier 7 — Production Arch      landing zones / multi-account / Terragrunt / drift
```

> Unlock each tier before advancing. Each node maps directly to real interview questions.

---

## 🏆 Achievement Badges

Earn and self-award as you complete milestones. Display them in your GitHub profile README.

| Badge | Unlock Condition |
|-------|-----------------|
| 🟢 FIRST APPLY | Complete Quest 1 |
| 📦 MODULE BUILDER | Build and call a reusable VPC module |
| 🔐 STATE GUARDIAN | Successfully recover from a corrupted tfstate |
| ⚡ PIPELINE RUNNER | Automate plan + apply via GitHub Actions |
| 🌍 MULTI-CLOUD OPS | Deploy same infra on AWS + GCP |
| 🚨 DRIFT BUSTER | Detect and reconcile infrastructure drift |
| 🛡️ POLICY ENFORCER | Add OPA / conftest policy gates to CI |
| 🏆 TERRAFORM ASSOCIATE | Pass HashiCorp Terraform Associate exam |
| 🤖 ATLANTIS RUNNER | Set up Atlantis for GitOps-style PR workflows |
| 🔴 LANDING ZONE ARCH | Complete Quest 6 — multi-account landing zone |

---

## 📋 Prerequisites

- Terraform CLI `>= 1.5` — [Install guide](https://developer.hashicorp.com/terraform/install)
- Git
- AWS / Azure / GCP account *(only from Quest 3 onwards — Quest 1 & 2 use local provider)*
- Optional: [LocalStack](https://localstack.cloud) for free AWS simulation

---

## 📖 Live Interactive Guide

The full gamified guide with quest cards, platform rankings, skill tree, and starter configs is live at:

**[terraform.eknathalabs.com](https://terraform.eknathalabs.com)**

---

## 🤝 Contributing

Found a bug? Have a better simulation scenario? PRs are welcome.

1. Fork the repo
2. Create your branch: `git checkout -b feat/your-scenario`
3. Commit: `git commit -m "feat: add [scenario name] simulation"`
4. Push and open a PR

---

## 📄 License

MIT © [EknathaLabs](https://eknathalabs.com) · [@eknatha](https://github.com/eknatha)

---

<p align="center">
  Built with 🔥 by <a href="https://eknathalabs.com">EknathaLabs</a> &nbsp;·&nbsp;
  <a href="https://terraform.eknathalabs.com">Live Guide</a> &nbsp;·&nbsp;
  <a href="https://github.com/eknatha">GitHub</a>
</p>
