# 📚 Team Engineering Standards & Guidelines

Welcome to the central documentation repository for our development team. This space defines the guidelines, naming conventions, Git workflows, and coding standards that all team members must follow across all organization projects.

---

## 📑 Table of Contents
- [1. Repository Naming Conventions](#1-repository-naming-conventions)
- [2. Directory & File Naming Rules](#2-directory--file-naming-rules)
- [3. Git Branching & Workflow](#3-git-branching--workflow)
- [4. Commit Message Standard (Conventional Commits)](#4-commit-message-standard-conventional-commits)
- [5. Environment Variables & Security](#5-environment-variables--security)
- [6. Team Identifiers](#6-team-identifiers)

---

## 1. Repository Naming Conventions

To keep our GitHub organization structured and searchable, all repositories outside the shared exercises space must follow a strict naming prefix.

### 🔹 Prefix Format
Every repository name must start with:
`[Member Prefix]-[Project Name]`

#### Member Prefixes:
* **`A`** = Alzate
* **`AP`** = Aparicio
* **`C`** = Carreño

---

### 💡 Naming Examples

#### Individual Projects:
* `c-web-portfolio` *(Carreño)*
* `a-algorithm-challenges` *(Alzate)*
* `ap-js-async-landing` *(Aparicio)*


---

## 2. Directory & File Naming Rules

To maintain uniformity across codebases, adhere strictly to these naming styles:

| Asset Type | Convention | Example |
| :--- | :--- | :--- |
| **Foldernames (Directories)** | `kebab-case` | `/src/user-management/` |
| **HTML / CSS files** | `kebab-case` | `index.html`, `main-styles.css` |
| **JavaScript / TypeScript files** | `camelCase` or `kebab-case` | `authController.ts`, `data-parser.js` |
| **React / Frontend Components** | `PascalCase` | `UserProfileCard.jsx`, `Navbar.tsx` |
| **Database Schemas / Models** | `PascalCase` or `snake_case` | `User.prisma`, `user_accounts.sql` |
| **Configuration files** | Lowercase | `.gitignore`, `.env.example`, `docker-compose.yml` |

---

## 3. Git Branching & Workflow

### 🌿 Branch Types
For shared repositories (`team-` projects), **never push directly to `main`**. Always work on feature or fix branches:

* **`main`**: Production-ready code. Protected branch.
* **`develop`**: Integration branch for upcoming releases.
* **`feature/[issue-id]-[description]`**: New features or modules.
  * Example: `feature/01-login-jwt`, `feature/user-dashboard`
* **`fix/[description]`**: Bug fixes.
  * Example: `fix/cors-header-error`
* **`chore/[description]`**: Tooling, config, or dependency updates.
  * Example: `chore/add-eslint-config`

---

## 4. Commit Message Standard (Conventional Commits)

We enforce [Conventional Commits](https://www.conventionalcommits.org/) for clean and readable commit histories.

### 📝 Format
`<type>(optional-scope): <short description in present tense>`

### 📌 Allowed Types:
* **`feat:`** A new feature for the user or application.
  * *Example:* `feat(auth): implement JWT token generation`
* **`fix:`** A bug fix.
  * *Example:* `fix(db): resolve connection timeout in PostgreSQL`
* **`docs:`** Documentation changes only.
  * *Example:* `docs: update setup steps in README`
* **`style:`** Changes that do not affect code meaning (white-space, formatting, semicolons).
  * *Example:* `style: apply prettier formatting to CSS`
* **`refactor:`** Code changes that neither fix a bug nor add a feature.
  * *Example:* `refactor(api): simplify user validation logic`
* **`test:`** Adding or updating tests.
  * *Example:* `test(unit): add unit tests for algorithm 1`
* **`chore:`** Updating build tasks, folder setups, package dependencies.
  * *Example:* `chore: initialize folder structure with .gitkeep`

---

## 5. Environment Variables & Security

1. **NO Secrets in Git:** Never commit `.env`, API keys, database credentials, or secret tokens.
2. **`.gitignore` Required:** Ensure every repository includes an updated `.gitignore` file before the first commit.
3. **`.env.example` Mandatory:** Always provide a `.env.example` file with mock/template keys so team members know which variables are required to run the project.

---

## 6. Team Identifiers

| Member | Full Name | Prefix | Primary IDE |
| :--- | :--- | :--- | :--- |
| **Alzate** | Member 1 | `A` | VS Code |
| **Aparicio** | Member 2 | `AP` | Antigravity |
| **Carreño** | Juan Carreño | `C` | WebStorm / PyCharm |

---

*Last Updated: October 2026 | Organization Engineering Standards*
