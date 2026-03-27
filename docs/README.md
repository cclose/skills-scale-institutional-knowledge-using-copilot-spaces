# OctoAcme — Project Management Overview

**Purpose:** Centralized, concise guide to OctoAcme project management processes used across initiatives. Use this as the single-page entry point to find more detailed process docs in this folder.

---

## Quick Start

When starting a new project or feature, follow the [Project Initiation guide](octoacme-project-initiation.md) to create a one-pager and confirm stakeholders.

## Core Roles

PM (coordinates delivery), PdM (defines outcomes), Developers, QA, Stakeholders. See [Roles & Personas](octoacme-roles-and-personas.md) for details.

## Team Rhythm

Daily standups, weekly delivery sync, sprint demos/reviews. See [Execution & Tracking](octoacme-execution-and-tracking.md).

## Key Workflows

- **Backlog & project board:** use Backlog → Ready → In Progress → In Review → QA → Done. See [Project Planning](octoacme-project-planning.md).
- **Pull Requests:** small PRs, include issue link and acceptance criteria, run CI and security scans before review. See [Execution & Tracking](octoacme-execution-and-tracking.md).

## Quality & Testing

Unit/integration tests, E2E smoke tests for critical flows, security scanning in CI. See [Execution & Tracking](octoacme-execution-and-tracking.md).

## Release & Deployment

Follow the release checklist before production deploys: deploy to staging, run smoke tests, have roll-forward/rollback plan ready. See [Release & Deployment](octoacme-release-and-deployment.md).

## Risk & Communication

Maintain a Risk Register, use the Weekly Status template for stakeholder updates, follow escalation paths for blockers. See [Risks & Communication](octoacme-risks-and-communication.md).

## Retrospectives & Continuous Improvement

Run after sprints/releases/incidents; capture action items and add to backlog. See [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md).

## Templates & Where to Add Content

Issue templates live in [`.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml`](../.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml) — use that template to request updates to these process docs.

## Using with Copilot Spaces

Add process-specific docs into `.copilot/` to make them available to Copilot Spaces. This repository already stores program process docs in `docs/` for that purpose.

---

*For a full narrative overview of all processes together, see [octoacme-project-management-overview.md](octoacme-project-management-overview.md).*
