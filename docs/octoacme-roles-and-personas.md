# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Using Personas for RACI / Ownership Decisions

Use the personas below when assigning ownership in a RACI matrix. Each persona maps to one or more RACI tags:

| Tag | Meaning |
|-----|---------|
| **R** | Responsible — does the work |
| **A** | Accountable — approves / owns the outcome |
| **C** | Consulted — provides input before decisions |
| **I** | Informed — kept up to date on progress |

**Example — Feature Deliverable:**

| Activity | PdM | Dev | QA | PM |
|----------|-----|-----|----|----|
| Feature scoped & accepted | A | C | C | I |
| Implementation complete | C | R | C | I |
| Test plan executed | I | C | R | I |
| Release approved | A | I | C | R |

> Copy the [Role Responsibility Template](templates/role-responsibility-template.md) to document per-project RACI assignments.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## UX Designer

### Role Summary
UX Designers are responsible for the user experience of OctoAcme products. They translate user needs and business goals into intuitive designs, from early wireframes through polished, developer-ready specifications.

### Responsibilities
- Conduct user research, usability tests, and accessibility reviews
- Create user flows, wireframes, prototypes, and high-fidelity mockups
- Define and maintain design standards and component libraries
- Provide implementation-ready assets and design specifications to Developers
- Review implemented UIs against design intent and flag regressions

### Goals
- Deliver experiences that are intuitive, accessible, and delightful
- Reduce design-development rework through early collaboration
- Advocate for the end user in every product decision

### Typical Communication
- Design reviews and critique sessions with Developers and PdMs
- Handoff notes and annotated prototypes in the design tool
- Usability findings shared as concise reports or story comments

### Interactions with existing roles
- **Product Managers**: collaborate on problem framing, user research, and acceptance criteria; PdM is Accountable, UX Designer is Responsible for design solutions.
- **Developers**: pair during implementation to clarify intent and review output; Developer is Responsible, UX Designer is Consulted.
- **Project Managers**: flag design-related scope changes or timeline risks; PM is Informed on design progress.
- **QA Engineers**: partner on accessibility and visual regression testing.

---

## Data Analyst

### Role Summary
Data Analysts define success metrics, build dashboards, and surface insights that guide product and engineering decisions. They ensure OctoAcme's features are instrumented correctly and that outcomes are measured rigorously.

### Responsibilities
- Define experiment metrics, KPIs, and success criteria in collaboration with PdMs
- Instrument features for analytics with Developer support
- Build and maintain dashboards and self-serve data tools
- Analyze usage data and experiment results; present findings and recommendations
- Maintain data quality standards and document data dictionaries

### Goals
- Enable data-driven decision-making across the team
- Reduce time-to-insight for post-release evaluation
- Ensure instrumentation is in place before features ship

### Typical Communication
- Written analysis reports and dashboard links shared in project channels
- Alignment sessions with PdMs prior to experiment launches
- Data-review meetings post-release

### Interactions with existing roles
- **Product Managers**: translate business questions into measurable hypotheses; PdM is Accountable, Data Analyst is Responsible for analysis.
- **Developers**: coordinate instrumentation and data pipeline work; Developer is Responsible, Data Analyst is Consulted.
- **Project Managers**: Informed on data readiness gates for release.
- **QA Engineers**: Consulted to validate that analytics events fire correctly in test environments.

---

## QA Engineer

### Role Summary
QA Engineers own quality assurance across the project lifecycle — from requirements review to post-release validation. They design and execute test strategies that give the team confidence to ship reliably.

### Responsibilities
- Develop and maintain test plans (functional, regression, smoke, exploratory)
- Implement and maintain automated test suites (unit, integration, E2E)
- Review acceptance criteria with PdMs and Developers before work begins
- Execute regression, smoke, and exploratory testing before each release
- Track and triage defects; advocate for quality standards across all phases

### Goals
- Catch defects as early as possible in the development cycle
- Enable continuous delivery through reliable automated test coverage
- Ensure every release meets the agreed Definition of Done

### Typical Communication
- Test plans and bug reports linked from sprint tickets
- Participation in sprint planning and backlog refinement
- Pre-release go/no-go signals shared with PM and PdM

### Interactions with existing roles
- **Developers**: collaborate on testability design and share ownership of automated tests; both are Responsible, QA leads strategy.
- **Product Managers**: consult on acceptance criteria and scope of testing; PdM is Accountable, QA is Consulted.
- **Project Managers**: provide release readiness status; PM is Informed.
- **Release Managers**: hand off test results and sign-off for production deployment.

> See the [QA & Release Checklists](checklists/qa-and-release-checklists.md) for the standard QA pre-release checklist.

---

## Release Manager

### Role Summary
Release Managers own the end-to-end release process — from planning deployment windows through post-release verification. They reduce release risk by coordinating all stakeholders and maintaining clear rollback plans.

### Responsibilities
- Maintain the release calendar and communicate deployment windows
- Coordinate release readiness reviews with QA, Developers, and PdMs
- Draft and publish release notes
- Manage rollback plans and ensure they are tested before each release
- Own post-deploy verification and incident escalation during releases

### Goals
- Achieve zero unplanned rollbacks by enforcing release gates
- Provide stakeholders with timely, accurate release status
- Continuously improve the release process based on retrospective findings

### Typical Communication
- Release readiness summaries distributed to all stakeholders
- Release calendar updates in project channels
- Incident notifications and post-mortems for any release failures

### Interactions with existing roles
- **QA Engineers**: receive test sign-off before proceeding; QA is Consulted, Release Manager is Accountable.
- **Developers**: coordinate code freeze and hotfix processes; Developer is Consulted.
- **Project Managers**: aligned on release milestones and risk; PM is Informed.
- **Product Managers**: confirm feature completeness and scope before release; PdM is Accountable for what ships.

> See the [QA & Release Checklists](checklists/qa-and-release-checklists.md) and [Release & Deployment Guide](octoacme-release-and-deployment.md) for detailed release process steps.

---

## Customer Support (Support Representative)

### Role Summary
Customer Support Representatives are the primary interface between OctoAcme's users and the product team. They surface real user pain points, escalate critical issues, and help maintain trust through timely, empathetic responses.

### Responsibilities
- Respond to user inquiries, bug reports, and escalations
- Document and triage incoming issues; route to engineering when needed
- Surface recurring pain points and feature gaps to PdMs
- Assist in drafting user-facing documentation, FAQs, and release communications
- Participate in pre-release walkthroughs to prepare support teams for new features

### Goals
- Resolve user issues quickly and accurately
- Reduce support ticket volume through proactive documentation and product improvements
- Build and maintain user trust and satisfaction

### Typical Communication
- Ticket summaries and trend reports shared with PdMs and Developers
- Participation in pre-release review sessions
- Escalation paging for critical production issues

### Interactions with existing roles
- **Product Managers**: regularly surface user feedback to inform prioritization; PdM is Accountable, Support is Consulted.
- **Developers**: relay production issues and reproduction steps; Developer is Responsible for fixes.
- **Project Managers**: Informed on escalations that may affect project timelines.
- **QA Engineers**: Consulted to validate bug fix coverage before releases.

---

## DevOps / Platform Engineer

### Role Summary
DevOps / Platform Engineers build and maintain the infrastructure, CI/CD pipelines, and tooling that enable OctoAcme teams to ship quickly and safely. They own platform reliability and developer productivity.

### Responsibilities
- Design, build, and operate CI/CD pipelines and deployment automation
- Manage infrastructure (cloud resources, environments, secrets)
- Define and enforce platform standards (containerization, observability, security baselines)
- Support Developers with tooling, environment issues, and platform onboarding
- Lead incident response for infrastructure and platform failures

### Goals
- Achieve high deployment frequency with low failure rates
- Minimize mean time to recovery (MTTR) for platform incidents
- Enable self-service for Developers while maintaining governance and security

### Typical Communication
- Runbooks and platform documentation in the project wiki
- On-call alerts and incident channels
- Office hours or async support channels for Developer queries

### Interactions with existing roles
- **Developers**: partner on CI/CD configuration, environment parity, and build optimization; both Responsible in their domains.
- **Release Managers**: provide deployment tooling and infrastructure readiness confirmations; DevOps is Responsible, Release Manager is Accountable.
- **Security/Compliance Lead**: implement security controls prescribed by the Security Lead; Security Lead is Consulted/Accountable on controls.
- **Project Managers**: Informed on infrastructure capacity and risk items.

---

## Security / Compliance Lead

### Role Summary
The Security / Compliance Lead ensures that OctoAcme products are built and operated securely and that the team meets all relevant regulatory and policy requirements. They embed security into the development lifecycle rather than treating it as a gate at the end.

### Responsibilities
- Define and maintain security policies, standards, and threat models
- Review architectures and code for security risks (shift-left security)
- Conduct or coordinate security testing (SAST, DAST, penetration testing)
- Ensure compliance with applicable regulations and policies (e.g., data privacy)
- Lead incident response for security events and own post-incident reviews

### Goals
- Prevent security incidents through proactive, embedded security practices
- Achieve and maintain compliance with all applicable standards
- Build a security-aware culture across the engineering team

### Typical Communication
- Security review findings shared with relevant teams prior to release
- Compliance status updates to leadership
- Incident reports and remediation tracking in secure channels

### Interactions with existing roles
- **Developers**: review code and architecture; Developer is Responsible for fixes, Security Lead is Accountable for standards.
- **DevOps / Platform Engineers**: define and validate infrastructure security controls; DevOps is Responsible, Security Lead is Accountable.
- **Product Managers**: Consulted on data handling and privacy implications of features.
- **Release Managers**: provide security sign-off as a release gate; Security Lead is Consulted, Release Manager is Accountable.

---

## Accessibility Advocate

### Role Summary
The Accessibility Advocate ensures that OctoAcme products are usable by people of all abilities. They champion inclusive design and technical standards, embedding accessibility into planning, design, implementation, and testing.

### Responsibilities
- Define and communicate accessibility standards (e.g., WCAG 2.1 AA) and acceptance criteria
- Review designs and implementations for accessibility compliance
- Conduct or coordinate assistive technology testing (screen readers, keyboard navigation, etc.)
- Provide training and guidance to Developers, UX Designers, and QA Engineers
- Track and prioritize accessibility defect remediation

### Goals
- Achieve and maintain WCAG 2.1 AA compliance across all surfaces
- Embed accessibility as a shared team responsibility, not a specialist gate
- Eliminate barriers that prevent any user from engaging with OctoAcme products

### Typical Communication
- Accessibility review reports shared alongside design and QA sign-off
- Training workshops and reference guides for the team
- Defect reports with severity classifications linked from sprint boards

### Interactions with existing roles
- **UX Designers**: partner from earliest concept stages; UX Designer is Responsible for accessible designs, Accessibility Advocate is Consulted/Accountable on standards.
- **Developers**: review implementations and recommend remediation; Developer is Responsible, Accessibility Advocate is Consulted.
- **QA Engineers**: align on accessibility test cases and incorporate into regression suites; QA is Responsible, Accessibility Advocate is Consulted.
- **Product Managers**: Consulted to ensure accessibility acceptance criteria are included in story definitions.

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Use the [RACI guidance](#using-personas-for-raci--ownership-decisions) above to assign ownership in project planning.
- Copy the [Role Responsibility Template](templates/role-responsibility-template.md) to document per-project role assignments.

