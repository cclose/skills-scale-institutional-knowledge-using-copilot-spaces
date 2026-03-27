# QA & Release Checklists

Use these checklists before every release to ensure quality and deployment readiness. Reference the [Release & Deployment Guide](../octoacme-release-and-deployment.md) for detailed process steps and the [Personas & Roles document](../octoacme-roles-and-personas.md) for role ownership.

---

## QA Checklist

**Owner:** QA Engineer (Responsible), Product Manager (Accountable)
**When to run:** Before the release readiness review; results shared with the Release Manager.

### Test Planning
- [ ] Test plan created and reviewed with Developers and PdM
- [ ] Scope of testing agreed (features in scope, explicit out-of-scope items documented)
- [ ] Test environments confirmed available and configured correctly
- [ ] Test data sets prepared and seeded in the test environment

### Automation
- [ ] Automated unit and integration tests pass in CI for all changed code
- [ ] End-to-end (E2E) automated test suite executed and results reviewed
- [ ] New automation coverage added for any net-new functionality
- [ ] Flaky tests investigated and resolved or tracked as known issues

### Regression Testing
- [ ] Regression suite executed for all impacted areas
- [ ] No high-severity or critical regressions identified (or documented exceptions approved by PdM)
- [ ] Cross-browser / cross-platform coverage verified per project requirements
- [ ] Performance baselines checked — no significant regressions introduced

### Acceptance Criteria Sign-Off
- [ ] All stories / tickets in scope have written acceptance criteria
- [ ] Acceptance criteria reviewed and validated with PdM during the sprint
- [ ] All acceptance criteria confirmed met (documented evidence or link to passing test cases)
- [ ] Accessibility checks completed against relevant WCAG criteria (see [Accessibility Advocate role](../octoacme-roles-and-personas.md#accessibility-advocate))
- [ ] QA Engineer has provided written go/no-go recommendation to Release Manager

---

## Release Checklist

**Owner:** Release Manager (Accountable), DevOps / Platform Engineer (Responsible for deployment execution)
**When to run:** Starting at the release readiness review; complete all items before production deployment.

### Pre-release Validation
- [ ] QA sign-off received (see QA Checklist above)
- [ ] Security sign-off received from Security / Compliance Lead (if applicable)
- [ ] All PRs merged to the release branch; no open, in-flight changes
- [ ] CI pipeline passes on the release branch (build, tests, security scans)
- [ ] Staging deployment completed and smoke tests passed
- [ ] Feature flags / toggles configured correctly for target environment
- [ ] Database migrations (if any) reviewed and tested in staging

### Rollback Plan
- [ ] Rollback procedure documented and reviewed with DevOps / Platform Engineer
- [ ] Rollback tested in staging or a lower environment (where feasible)
- [ ] Rollback trigger criteria defined (e.g., error rate threshold, P1 bug)
- [ ] On-call rotation confirmed and contacts shared with all stakeholders

### Release Notes
- [ ] Release notes drafted covering all changes included in the release
- [ ] Release notes reviewed and approved by PdM
- [ ] User-facing copy (if any) reviewed by Customer Support for accuracy and tone
- [ ] Internal announcement drafted for stakeholders (PM, leadership, support team)

### Post-deploy Checks
- [ ] Production deployment completed with no unexpected errors
- [ ] Post-deploy smoke tests executed and passed in production
- [ ] Key monitoring dashboards checked (error rates, latency, key metrics)
- [ ] Analytics instrumentation verified (events firing correctly in production)
- [ ] Release notes and announcements published to stakeholders
- [ ] Any outstanding known issues documented and tracked in the backlog
- [ ] Deployment retrospective / debrief scheduled (for major releases)

---

## Related Resources
- [Release & Deployment Guide](../octoacme-release-and-deployment.md)
- [Role Responsibility Template](../templates/role-responsibility-template.md)
- [OctoAcme Personas & Roles](../octoacme-roles-and-personas.md)
