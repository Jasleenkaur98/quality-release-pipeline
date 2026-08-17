# 🚀 Quality & Release Pipeline Framework

![CI Quality Gate](https://github.com/Jasleenkaur98/quality-release-pipeline/actions/workflows/ci-quality-gate.yml/badge.svg)

An enterprise-grade CI/CD release orchestration repository featuring automated quality gates, environment management, performance optimizations, and semantic release controls.

## 🛠️ Tech Stack & Tools
- **CI/CD Platform:** GitHub Actions
- **Security Audit:** `npm audit`
- **Environment Matrix:** Node.js (18, 20, 22) on Ubuntu Latest
- **Hosting / Deployment:** GitHub Pages
- **Release Automation:** `softprops/action-gh-release` + Semantic Version Tags (`v*.*.*`)

---

## ⚙️ Pipeline Architecture

[ Push / PR to main ]
│
▼
┌──────────────────┐
│ Security Audit   │ ──► npm audit (Vulnerability Scanning)
└─────────┬────────┘
│
▼
┌──────────────────┐
│ Test Matrix      │ ──► Concurrent runs on Node.js 18, 20, & 22 (npm cache enabled)
└─────────┬────────┘
│
▼
┌──────────────────┐
│ Package Artifact │ ──► Generate distribution build & upload pipeline artifacts
└─────────┬────────┘
│
▼
┌──────────────────┐
│ CD Deployment    │ ──► Deploy live static application to GitHub Pages
└──────────────────┘

---

## 🛡️ Enterprise Guardrails & Performance
- **Dependency Caching:** Integrated `actions/cache` for npm dependencies to significantly reduce pipeline execution times.
- **Semantic Releases:** Automatic production releases with auto-generated release notes triggered on `v*.*.*` tags.
- **Branch Protection:** Enforced required status checks before merging code into `main`.
- **Failure Alerts:** Native error handling and GitHub notifications triggered on workflow failures.