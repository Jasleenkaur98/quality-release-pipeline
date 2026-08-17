# 🚀 Quality & Release Pipeline Framework

![CI Quality Gate](https://github.com/Jasleenkaur98/quality-release-pipeline/actions/workflows/ci-quality-gate.yml/badge.svg)

An enterprise-grade CI/CD release orchestration repository featuring automated quality gates, environment management, performance optimizations, and semantic release controls.

## 🛠️ Tech Stack & Tools
- **CI/CD Platform:** GitHub Actions
- **Security Audit:** `npm audit`
- **Environment Matrix:** Node.js (18, 20, 22) on Ubuntu Latest
- **Hosting / Deployment:** GitHub Pages
- **Release Automation:** `softprops/action-gh-release` + Semantic Version Tags (`v1.0.0`)

---

## ⚙️ Pipeline Architecture

| Stage | Trigger / Action | Output |
| :--- | :--- | :--- |
| **1. Trigger** | Code `push` or `pull_request` to `main` | Workflow execution initialized |
| **2. Security Audit** | Runs `npm audit` scanning dependencies | Vulnerability report generated |
| **3. Test Matrix** | Concurrent execution across Node 18, 20, & 22 | Cached dependency verification & unit tests |
| **4. Package Build** | Bundles production distribution files | Uploads artifact `production-build` |
| **5. CD Deployment** | Triggers GitHub Pages deployment action | Application live on public URL |

---

## 🛡️ Enterprise Guardrails & Performance
- **Dependency Caching:** Integrated `actions/cache` for npm dependencies to significantly reduce pipeline execution times.
- **Semantic Releases:** Automatic production releases with auto-generated release notes triggered on `v1.0.0` tags.
- **Branch Protection:** Enforced required status checks before merging code into `main`.
- **Failure Alerts:** Native error handling and GitHub notifications triggered on workflow failures.