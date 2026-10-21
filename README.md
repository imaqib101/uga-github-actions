# GitHub Actions CI/CD Blueprint Hub ⚙️

[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-Automated%20Pipelines-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/features/actions)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-Zero--Touch%20Deploys-44cc11?style=for-the-badge)](https://en.wikipedia.org/wiki/CI/CD)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

A curated collection of production-grade **GitHub Actions workflow templates** and CI/CD automation pipelines for modern web applications, frontend monorepos, and backend microservices.

---

## 🚀 Workflow Library

| Workflow | Target | Capabilities |
| :--- | :--- | :--- |
| **`ci-frontend.yml`** | Vue / React / Next.js | Type-check, ESLint, Prettier, Vitest coverage |
| **`ci-backend.yml`** | Node.js / Express / APIs | Integration tests, security audit, database containers |
| **`docker-publish.yml`** | Containerized Services | Multi-arch Docker build & push to GitHub Container Registry (GHCR) |
| **`release-drafter.yml`** | SemVer Automation | Automated changelog generation and GitHub Release tagging |

---

## 📋 Included Template: Modern Frontend CI

```yaml
name: Frontend CI

on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: "pnpm"
      - run: pnpm install --frozen-lockfile
      - run: pnpm lint
      - run: pnpm type-check
      - run: pnpm test:run
```

---

## 👤 Author

**Mohammed Aqib**
- GitHub: [@imaqib101](https://github.com/imaqib101)
- Location: Bengaluru, India
