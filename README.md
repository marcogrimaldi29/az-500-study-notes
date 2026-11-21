# 🔐 AZ-500: Microsoft Azure Security Technologies
### Study Notes Repository

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?logo=github)](https://marcogrimaldi29.com/az-500-study-notes/)
[![marcogrimaldi29.com](https://img.shields.io/badge/Blog-marcogrimaldi29.com-red?logo=rss)](https://marcogrimaldi29.com)

> [!WARNING]
> **AZ-500 retired on 31 August 2026.** Microsoft retired the exam, the Microsoft Certified: Azure Security Engineer Associate certification and its renewal assessment, so they can no longer be taken or renewed. These notes stay online as an archived reference. The successor is **[SC-500: Microsoft Certified: Cloud and AI Security Engineer Associate](https://learn.microsoft.com/en-us/credentials/certifications/cloud-and-ai-security-engineer-associate/)**; see [Retirement & Successor](#retirement-and-successor).

> 🎯 **Original goal:** Earn the Microsoft Certified: Azure Security Engineer Associate badge *(no longer possible since 31 August 2026)*
> 📅 **Notes Version:** 2026, final AZ-500 skills outline (22 January 2026), archived
> 🌐 **Published site:** [📘 AZ-500 Study Notes](https://marcogrimaldi29.com/az-500-study-notes/)
> ✍️ **Author:** [Marco Grimaldi](https://www.linkedin.com/in/marco-grimaldi29/)

---

## 📋 Exam At-a-Glance

| Detail | Info |
|--------|------|
| 🏅 Certification | Microsoft Certified: Azure Security Engineer Associate |
| 🗄️ Status | **Retired on 31 August 2026** (exam, certification and renewal assessment) |
| ➡️ Successor | **SC-500**: Microsoft Certified: Cloud and AI Security Engineer Associate |
| 📝 Passing Score | **700 / 1000** |
| 💶 Exam Price | No longer offered *(was ~€126 EUR, varied by region)* |
| ⏱️ Duration | **~100 minutes** |
| ❓ Question Types | MCQ, multi-select, drag-and-drop, case studies |
| 🔁 Renewal | No longer available. Existing certifications stay valid until they expire *(was annual, via a free online assessment)* |

---

## 📊 Official Domain Breakdown (final)

```mermaid
pie title AZ-500 Exam Domain Weights (final)
    "Secure Identity & Access (15–20%)" : 20
    "Secure Networking (20–25%)" : 25
    "Secure Compute, Storage & Databases (20–25%)" : 25
    "Defender for Cloud & Sentinel (30–35%)" : 30
```

| # | Domain | Official Weight | Key Services |
|---|---------|----------------|--------------|
| 1 | Secure Identity & Access | **15–20%** | Entra ID, PIM, MFA, Conditional Access, Managed Identities |
| 2 | Secure Networking | **20–25%** | NSG, ASG, Firewall, WAF, Private Endpoint, DDoS |
| 3 | Secure Compute, Storage & Databases | **20–25%** | ADE, AKS, ACR, TDE, Key Vault, SQL Auditing |
| 4 | Defender for Cloud & Microsoft Sentinel | **30–35%** | Defender plans, Secure Score, SIEM, SOAR, Automation |

> 🔑 **Domain 4 = heaviest domain** — allocate ≥35% of total study time here.

---

## 🗺️ Certification Path

AZ-500 is retired and SC-500 replaces it, including as a prerequisite option for the Cybersecurity Architect Expert certification.

```mermaid
flowchart LR
    AZ900["☁️ AZ-900<br>Azure Fundamentals<br>(optional foundation)"]
    SC900["🪪 SC-900<br>Security, Compliance, and<br>Identity Fundamentals<br>(optional foundation)"]
    AZ500["🔐 AZ-500<br>Azure Security Engineer Associate<br>❌ Retired 31 Aug 2026"]
    SC500["🛡️ SC-500<br>Cloud and AI Security<br>Engineer Associate<br>(successor)"]
    SC200["📡 SC-200<br>Security Operations<br>Analyst Associate"]
    SC300["🪪 SC-300<br>Identity and Access<br>Administrator Associate"]
    SC100["🏛️ SC-100<br>Cybersecurity Architect Expert"]

    AZ900 -->|Foundation| SC500
    SC900 -->|Foundation| SC500
    AZ500 -.->|"Replaced by"| SC500
    SC500 -->|"Prerequisite (one of)"| SC100
    SC200 -->|"Prerequisite (one of)"| SC100
    SC300 -->|"Prerequisite (one of)"| SC100

    classDef retired stroke-dasharray:5 5,color:#888
    class AZ500 retired
```

---

<a id="retirement-and-successor"></a>
## 🗄️ Retirement & Successor (SC-500)

Microsoft retired the AZ-500 exam, the Microsoft Certified: Azure Security Engineer Associate certification and its renewal assessment on **31 August 2026 at 11:59 PM Central Standard Time**. The direct replacement is **Exam SC-500: Implementing End-to-End Security Controls for Cloud and AI Workloads**, which earns **Microsoft Certified: Cloud and AI Security Engineer Associate** (generally available since 21 July 2026).

- **Already certified?** Your AZ-500 certification stays valid, and on your Microsoft Learn transcript, until it expires. It can't be renewed.
- **SC-500 domains:** Manage identity, access, and governance (20–25%) · Secure storage, databases, and networking (25–30%) · Secure compute, now including security for AI (20–25%) · Manage and monitor security posture (20–25%).
- **New in SC-500:** security for AI and agents (Purview DSPM, Defender for AI Services, Microsoft Entra Agent ID, Microsoft Foundry guardrails), Microsoft Security Copilot, Microsoft Entra Private Access, Azure Arc and Azure Machine Configuration.
- **SC-100 prerequisite:** Cybersecurity Architect Expert now requires one of SC-300, SC-200 or SC-500. AZ-500 is no longer listed.

The [site's Home page](https://marcogrimaldi29.com/az-500-study-notes/#retirement-and-successor) has the full domain comparison. Sources: [AZ-500 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-500) · [SC-500 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-500) · [Exam and assessment lab retirement](https://learn.microsoft.com/en-us/credentials/support/retired-certification-exams) · [Cybersecurity Architect Expert prerequisites](https://learn.microsoft.com/en-us/credentials/certifications/cybersecurity-architect-expert/#certification-prerequisites)

---

## 🗂️ Repository Structure

```
az-500-study-notes/
├── README.md                             ← 📍 You are here
├── index.md                              ← GitHub Pages home
├── 00-azure-security-fundamentals.md     ← Core security concepts & Zero Trust
├── 01-identity-access.md                 ← Domain 1: Identity & Access (15–20%)
├── 02-secure-networking.md               ← Domain 2: Secure Networking (20–25%)
├── 03-compute-storage-databases.md       ← Domain 3: Compute/Storage/DB (20–25%)
├── 04-defender-sentinel.md               ← Domain 4: Defender + Sentinel (30–35%)
└── 05-quick-reference-cheatsheet.md      ← Last-minute review & exam traps
```

---

## 📚 Official Learning Resources

| Resource | Link |
|----------|------|
| 📄 Official Exam Page *(retired)* | [AZ-500 Exam](https://learn.microsoft.com/en-us/credentials/certifications/azure-security-engineer/) |
| 📋 Study Guide *(retired)* | [Official AZ-500 Study Guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-500) |
| 🧪 Free Practice Assessment *(retired exam)* | [AZ-500 Practice Assessment](https://learn.microsoft.com/en-us/credentials/certifications/azure-security-engineer/practice/assessment?assessment-type=practice&assessmentId=57) |
| 🆕 Successor Certification | [SC-500: Cloud and AI Security Engineer Associate](https://learn.microsoft.com/en-us/credentials/certifications/cloud-and-ai-security-engineer-associate/) |
| 📋 Successor Study Guide | [SC-500 Study Guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-500) |
| 🗓️ Retired Exams List | [Exam and assessment lab retirement](https://learn.microsoft.com/en-us/credentials/support/retired-certification-exams) |
| 🎬 Exam Readiness Videos | [Exam Readiness Zone](https://learn.microsoft.com/en-us/shows/exam-readiness-zone/?terms=AZ-500) |
| 🔐 Microsoft Defender for Cloud | [Defender Docs](https://learn.microsoft.com/en-us/azure/defender-for-cloud/) |
| 🗡️ Microsoft Sentinel | [Sentinel Docs](https://learn.microsoft.com/en-us/azure/sentinel/) |
| 🏛️ Azure Security Benchmark | [MCSB](https://learn.microsoft.com/en-us/security/benchmark/azure/) |

---

### ✅ Key Study Tips

These were written for AZ-500. Most of them still apply to SC-500's identity, networking and posture-management domains.

- 🎯 The exam tests **"why this control?"** — think in threat models and defence-in-depth layers
- 🔄 Understand **Zero Trust principles** — verify explicitly, least privilege, assume breach
- 🔑 Know **Key Vault tiers** (Standard vs Premium/HSM) and when to use each
- 🛡️ **Defender for Cloud Secure Score** is heavily tested — know how to interpret & improve it
- 📊 Memorise **RBAC built-in roles** vs custom roles, and when each is appropriate
- 🌐 Know **all Private Endpoint vs Service Endpoint trade-offs** — scenario questions test these
- 🔍 Understand **Microsoft Sentinel analytics rule types** (Scheduled, NRT, Fusion, etc.)
- ⚡ **PIM** — know the difference between eligible, active, and permanent assignments

---

## 📚 About the Study Notes

These notes are hosted on **GitHub Pages** and published as a searchable website on this URL:

👉 **[📘 AZ-500 Study Notes](https://marcogrimaldi29.com/az-500-study-notes/)**

The site includes full-text search, Mermaid diagram rendering, and mobile-friendly navigation for on-the-go review. 

These notes are designed to be a structured, exam-focused summary of the most important concepts and services based on the official [Microsoft AZ-500 Study Guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-500) and its criteria. They follow the final AZ-500 skills outline (22 January 2026) and are kept as an archived reference now that the exam has retired.

Additional study notes maintained by me are also available for those pursuing Microsoft and Azure certifications at the following Landing Page:

👉 **[🛬 Landing Page: Study Notes](https://marcogrimaldi29.com/study-notes/)**

---

## ✍️ About the Author

Maintained by **[Marco Grimaldi](https://www.linkedin.com/in/marco-grimaldi29/)** — Cloud Consultant, Language Trainer & Lifelong Learner.

Find more certification guides, study tips, and tech content at **[🏠 marcogrimaldi29.com](https://marcogrimaldi29.com)**

The site is continuously updated and based on my personal study notes and experiences. If you have any feedback, suggestions, or corrections, feel free to [reach out](https://marcogrimaldi29.com/contact/)!

---

## 📈 Analytics

This site uses [Umami](https://umami.is/) for privacy-friendly analytics.

---

## 🐞 Spotted a Mistake?

Azure security services change fast, so if something here is wrong or out of date, please [report an issue](https://github.com/marcogrimaldi29/az-500-study-notes/issues).

---

## 💚 Support

If these notes helped you prepare for AZ-500, there are a couple of ways to show it: ⭐ star this repo on GitHub so other candidates can find it, or 🤝 connect with me on LinkedIn.

<p>
  <a href="https://github.com/marcogrimaldi29/az-500-study-notes"><img src="https://img.shields.io/badge/Star_on_GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="Star on GitHub" /></a>
  <a href="https://www.linkedin.com/in/marco-grimaldi29/"><img src="https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMC40NDcgMjAuNDUyaC0zLjU1NHYtNS41NjljMC0xLjMyOC0uMDI3LTMuMDM3LTEuODUyLTMuMDM3LTEuODUzIDAtMi4xMzYgMS40NDUtMi4xMzYgMi45Mzl2NS42NjdIOS4zNTFWOWgzLjQxNHYxLjU2MWguMDQ2Yy40NzctLjkgMS42MzctMS44NSAzLjM3LTEuODUgMy42MDEgMCA0LjI2NyAyLjM3IDQuMjY3IDUuNDU1djYuMjg2ek01LjMzNyA3LjQzM2EyLjA2MiAyLjA2MiAwIDAgMS0yLjA2My0yLjA2NSAyLjA2NCAyLjA2NCAwIDEgMSAyLjA2MyAyLjA2NXptMS43ODIgMTMuMDE5SDMuNTU1VjloMy41NjR2MTEuNDUyek0yMi4yMjUgMEgxLjc3MUMuNzkyIDAgMCAuNzc0IDAgMS43Mjl2MjAuNTQyQzAgMjMuMjI3Ljc5MiAyNCAxLjc3MSAyNGgyMC40NTFDMjMuMiAyNCAyNCAyMy4yMjcgMjQgMjIuMjcxVjEuNzI5QzI0IC43NzQgMjMuMiAwIDIyLjIyNSAweiIvPjwvc3ZnPg%3D%3D" alt="Connect on LinkedIn" /></a>
</p>

---

## ©️ Credits & Acknowledgements

The **[Just the Docs](https://github.com/just-the-docs/just-the-docs)** theme is used for a clean documentation-style layout. Licensed under [MIT](https://opensource.org/license/MIT).

**[Claude Sonnet 4.6](https://www.anthropic.com/news/claude-sonnet-4-6)** was used for initial content generation; all final edits, fact-checking, and formatting by the author.

> *Not affiliated with or endorsed by Microsoft. Always verify against the latest Microsoft documentation.*
