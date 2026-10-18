# ci-cd.md

> Optional. Fill this in only if the project needs automated checks or deployment.

---
## AI RULES — READ FULLY BEFORE ANY ACTION
---

1. If "Needed" below is No → do nothing. If it is blank → ask the human.
   Never set up a pipeline on your own.
2. Read this entire file and architecture-notes.md before creating or
   changing any pipeline.
3. Match the project scale. Do not add steps, tools, or environments
   the project does not need.
4. Never touch secrets, credentials, or production config without
   human approval. Never put secrets in the repo.
5. Never deploy to production without human confirmation.
6. Log hard-to-reverse choices (platform, deploy strategy) in
   decision-log.md, following its filter.

---
## WHAT THIS IS
---

**CI (continuous integration):** every change is automatically checked
(lint, tests, build) before it is accepted.

**CD (continuous delivery / deployment):** a change that passes is
automatically shipped to an environment, without manual steps.

**Usually worth it when:** more than one person contributes, the code is
deployed repeatedly, tests exist, or manual deploys cause mistakes.

**Usually not needed when:** it is a solo prototype, there are no tests,
or it is deployed rarely.

---
## PROJECT REFERENCE
---

**Needed:**
[ ] Yes   [ ] No   [ ] Later

**Platform:**
(e.g. GitHub Actions, GitLab CI)

**Checks on every change:**
(e.g. lint, type check, tests, build)

**Environments:**
(e.g. staging, production)

**Deploy trigger:**
(e.g. merge to main, manual approval, tagged release)

**Deploy target:**
(host or platform)

**Where secrets are stored:**
(never in the repo)

**Must never run automatically:**
(e.g. production deploys, database migrations)

**Known fragile steps:**

---
