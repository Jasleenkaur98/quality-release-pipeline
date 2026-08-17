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

```mermaid
graph TD
    A[Push / PR to main] --> B[Security Audit: npm audit]
    B --> C[Test Matrix: Node.js 18, 20, 22]
    C --> D[Package Artifact: Production Build]
    D --> E[CD Deployment: GitHub Pages]# 🚀 Quality & Release Pipeline Framework

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

```mermaid
graph TD
    A[Push / PR to main] --> B[Security Audit: npm audit]
    B --> C[Test Matrix: Node.js 18, 20, 22]
    C --> D[Package Artifact: Production Build]
    D --> E[CD Deployment: GitHub Pages]


    🛡️ Enterprise Guardrails & Performance
Dependency Caching: Integrated actions/cache for npm dependencies to significantly reduce pipeline execution times.

Semantic Releases: Automatic production releases with auto-generated release notes triggered on v1.0.0 tags.

Branch Protection: Enforced required status checks before merging code into main.

Failure Alerts: Native error handling and GitHub notifications triggered on workflow failures.