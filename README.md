# Git-Flows Project

## Project Overview

This repository demonstrates a practical implementation of the GitFlow workflow, showcasing feature branching, release management, and the use of Git hooks for automation. The project covers the full lifecycle of development from initializing GitFlow to creating feature and release branches, handling merges and conflicts, and automating commit and merge validations with Git hooks.

---

## Table of Contents

- [Project Setup](#project-setup)
- [Feature Branching](#feature-branching)
- [Release Process](#release-process)
- [Git Hooks and Automation](#git-hooks-and-automation)
- [Repository Structure](#repository-structure)
- [How to Use](#how-to-use)

---

## Project Setup

- Installed `git-flow` to facilitate branching workflows.
- Created an empty GitHub repository named `ALXprodev-advanced_git`.
- Cloned the repository locally.
- Created a `develop` branch to separate ongoing development from production.
- Pushed the `develop` branch to the remote repository.
- Initialized GitFlow with default settings (`git flow init -d`).
- Added an initial empty `README.md` file, committed, and pushed to `develop`.

---

## Feature Branching

- Created a feature branch `feature/implement-login` from `develop`.
- Added a directory `login-page` with a `README.md` stating "Login Feature Coming soon".
- Committed changes with message:
  `feat: scaffolding login page`
- Pushed the feature branch to GitHub to isolate feature work from main development.

---

## Release Process

- Created another feature branch `feature/implement-signup` from `develop`.
- Added a directory `signup-page` with a `README.md` containing "feature coming soon".
- Committed and pushed changes to GitHub.
- Merged both feature branches back into `develop`, resolving any conflicts.
- Created a release branch `release/1.0.0` from `develop` to prepare for production.
- Updated `signup-page/README.md` in the release branch by adding:
  `data requirements: email, firstName, lastName, profilePic`
- Committed and pushed the release branch.
- Merged the release branch into both `main` (production) and `develop` branches to keep them in sync.
- Tagged the release with `v1.0.0` and pushed tags to the remote repository.

---

## Git Hooks and Automation

- Implemented a `pre-commit` Git hook to enforce repository standards:
  - Checks that every directory contains a `README` or `README.md` file before allowing a commit.
- Implemented a `post-merge` Git hook to log merges on the `main` branch:
  - Logs merge events with timestamps to a `merge_log.txt` file for audit purposes.
- These hooks improve code quality and provide traceability during the GitFlow process.

---

## Repository Structure

ALXprodev-advancedgit/
├── login-page/
│ └── README.md
├── signup-page/
│ └── README.md
├── README.md

---

## How to Use

1. Clone the repository.
2. Use GitFlow commands to create feature, release, and hotfix branches as per project requirements.
3. Ensure commit standards using the provided Git hooks.
4. Review logs in `merge_log.txt` for merge auditing on the `main` branch.
5. Push changes and tags to keep remote repository updated and maintain a clean history.

---
