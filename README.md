# Quality & Release Pipeline Framework

![CI Quality Gate](https://github.com/Jasleenkaur98/quality-release-pipeline/actions/workflows/ci-quality-gate.yml/badge.svg)

A modern CI/CD release orchestration repository featuring automated quality gates, environment management, and release controls.

## 🚀 Pipeline Status
- **CI Workflow:** Active (`ci-quality-gate.yml`)
- **Quality Gates:** Fully Operational (Security + Test Matrix + Packaging)

## ⚙️ Workflow Architecture
- **Trigger:** Automated execution on `push` and `pull_request` to `main`.
- **Environment:** Ubuntu Latest runner with Node.js matrix runtime.
- **Quality Checks:** 
  - **Dependency Audit:** Security vulnerability scanning via `npm audit`.
  - **Test Matrix:** Concurrent unit testing on Node.js 18, 20, and 22.
  - **Artifact Packaging:** Automatic build generation and storage on `main` merge.

  ## 🛡️ Enterprise Guardrails & Performance
- **Caching:** Integrated `actions/cache` for npm dependencies to optimize build times.
- **Semantic Releases:** Automatic release creation with changelogs triggered on `v*.*.*` tags.
- **Branch Protection:** Enforced status checks and PR reviews on the `main` branch.
- **Failure Handling:** Built-in alert hooks on job failures.