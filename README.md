# A301-CodePath-MCGILL
CodePath X Github Open-source contribution for MCGILL

# Contribution [#346]: French Translation Support

**Contribution Number:** [2]  
**Student:** Imran (NYAN LIN ZAW)  
**Issue:** https://github.com/mcgill-courses/mcgill.courses/issues/346  
**Status:** Phase I – In Progress

---

**Fork link:** [https://github.com/MImran2002/mcgill.courses]

## Why I Chose This Issue

I chose this issue because it combines internationalization (i18n), front-end architecture, and React. While the issue initially appears to be about adding French translation support, implementing localization requires designing a solution that is scalable rather than simply translating individual strings. I tried doing that with a universal design system at my internship too so I am excited for this too.

I also wanted to gain experience working with a modern production React application that uses Rust, Vite, TypeScript, MongoDB, and Docker. Since McGill University serves both English- and French-speaking students, this issue provides an opportunity to improve accessibility while learning how internationalization is introduced into an existing codebase through a new library which I have no clue about.

Because the issue description leaves the implementation scope open-ended, I also wanted to practice communicating with project maintainers. Before beginning implementation, I reached out to clarify whether the goal is to establish the internationalization infrastructure first or to translate the entire application.

---

## Understanding the Issue

### Problem Description

The application currently serves its interface in English only. The issue proposes introducing French translation support using `react-i18next` to better accommodate McGill University's bilingual community. At the time development began, the exact implementation scope had not yet been clarified as I have commented - 
"Working on this now, @terror!

I had a quick question about the scope of this issue. When you say "add a French translation," are you envisioning:

Adding the internationalization (i18n) infrastructure (e.g., react-i18next) and translating a small set of UI components as a starting point, with the rest of the app migrated over time, or

Refactoring the entire frontend so that all user-facing strings are translatable and providing a complete French translation?

I just want to make sure I approach the implementation in the direction you have in mind before I get too far."

### Expected Behavior

The application should support an internationalization framework that enables text to be translated into French.

### Current Behavior

The application currently displays text in English, and no internationalization framework has been integrated.

### Affected Components

Based on the issue description, localization may affect:

- Application initialization
- Navigation components
- Shared UI components
- Individual pages
- Components containing hard-coded user-facing strings

---

## Reproduction Process

### Environment Setup

**Operating System:** macOS (Apple Silicon)

**Rust Version:** Installed through Cargo

**Docker:** Installed

**MongoDB:** Local Docker Compose instance

**Node Version:** v26.4.0

**pnpm Version:** 11.1.2

**Setup Notes:**

- Forked the `mcgill.courses` repository and cloned it locally.
- Reviewed the project documentation and identified the required development tools and technologies.
- Started MongoDB using Docker Compose.
- Successfully compiled the Rust backend.
- Discovered that the README referenced an outdated backend startup command using the `serve` subcommand.
- Investigated the project's CLI help output and identified the correct startup command:
  ```bash
  cargo run -- --source=seed --initialize --db-name=mcgill-courses
  ```
- Successfully initialized and seeded the local MongoDB database.
- Upgraded Node.js from version 20 to version 26 after identifying compatibility issues with pnpm.
- Investigated and resolved PATH conflicts caused by multiple Homebrew Node installations.
- Installed all frontend dependencies using pnpm.
- Successfully launched the React frontend using Vite.
- Verified that both the backend and frontend were running locally.
- Created the feature branch `frenchSiteTranslation`.
- Explored the frontend architecture, including `main.tsx`, `app.tsx`, routing, and provider organization to determine how internationalization should be integrated.
- Installed `i18next` and `react-i18next` in preparation for implementation.
- Contacted the project maintainer to clarify the expected scope before beginning implementation.

### Steps to Reproduce

1.

2.

3.

4.

5.

### Reproduction Evidence

- **Commit showing reproduction:**
- **Screenshots/logs:**
- **My findings:** Successfully configured and launched the complete local development environment. While preparing to implement the feature, I determined that the implementation scope should first be clarified with the project maintainer before modifying the application architecture.

---

## Solution Approach

### Analysis

The issue proposes adding French localization using `react-i18next`, but does not specify whether the objective is to establish the localization infrastructure or fully translate the application.

### Proposed Solution

Introduce an extensible internationalization framework that supports future language additions while preserving the existing application architecture.

### Implementation Plan

#### Understand

Reviewed the issue description and project documentation.

#### Match

Examined the application architecture, including routing, providers, and frontend entry points.

#### Plan

Prepared the local development environment and identified where localization should be introduced.

#### Implement

#### Review

#### Evaluate

---

## Testing Strategy

### Unit Tests

### Integration Tests

Verified that the Rust backend, MongoDB, and React frontend all run successfully in the local development environment.

### Manual Testing

Confirmed that the backend initializes correctly, the database is seeded successfully, and the frontend launches through Vite.

---

## Implementation Notes

### Week 1 Progress

- Forked and cloned the repository.
- Configured the complete local development environment.
- Started MongoDB using Docker Compose.
- Compiled the Rust backend.
- Identified outdated startup instructions in the project README.
- Investigated the backend CLI and determined the correct startup command.
- Successfully initialized and seeded the local database.
- Upgraded Node.js to resolve pnpm compatibility issues.
- Diagnosed and resolved PATH conflicts caused by multiple Node.js installations.
- Installed frontend dependencies.
- Successfully launched the frontend using Vite.
- Created a dedicated feature branch.
- Explored the frontend architecture to understand where internationalization should be integrated.
- Installed `i18next` and `react-i18next`.
- Contacted the project maintainer to clarify the expected implementation scope before making code changes.

Backend Successfully running: <img width="410" height="381" alt="image" src="https://github.com/user-attachments/assets/1877fce4-f2d5-4153-8c97-2297df8b221b" />

Frontend Successfully running: <img width="769" height="535" alt="image" src="https://github.com/user-attachments/assets/e26974a1-c85e-485c-9bb9-061c52a8dbdb" />

### Week 2 Progress

### Week 3 Progress

### Code Changes

- **Files modified:**
- **Key commits:**
- **Approach decisions:** Delayed implementation until the project maintainer clarifies whether the issue should introduce localization infrastructure or fully translate the application.

---

## Pull Request

**PR Link:**

### PR Description

### Maintainer Feedback

**Status:** Not yet opened

---

## Learnings & Reflections

### Technical Skills Gained

- Rust project setup and compilation.
- MongoDB development using Docker Compose.
- React application architecture.
- Vite development workflow.
- pnpm workspace management.
- Homebrew package management.
- Node.js environment troubleshooting.
- Development environment configuration for large open-source projects.
- Open-source contribution workflow, including issue analysis, environment setup, architecture investigation, and maintainer communication.

### Challenges Overcome

- Resolved Node.js and pnpm version compatibility issues.
- Diagnosed PATH conflicts created by multiple Homebrew Node.js installations.
- Corrected outdated project startup instructions through investigation of the application's CLI.
- Successfully configured the backend, frontend, and database to work together locally.

### What I'd Do Differently Next Time

For feature requests with an open-ended description, I would clarify the expected implementation scope with the project maintainer before beginning architectural changes.

---

## Resources Used

- McGill Courses Issue #346
- Project README
- Cargo CLI help output
- Docker Compose
- Homebrew
- pnpm Documentation
- ChatGPT
- Claude
