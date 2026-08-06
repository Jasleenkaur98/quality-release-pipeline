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