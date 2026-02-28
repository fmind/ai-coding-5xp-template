# Workflow Process

This document defines how the engineering and product teams collaborate to deliver features for ActiveGear.

## Agile Methodology

- **Sprint Cycles**: The team operates on two-week sprint cycles, finishing with a sprint review emphasizing working software over presentation slides.
- **Daily Stand-ups**: Brief (15-minute max) daily meetings focused on blockers and alignment, rather than status reporting.
- **Retrospectives**: Dedicated time at the end of each sprint to identify process improvements, focusing on actionable "blameless" takeaways.

## Feature Delivery

- **A/B Testing**: New user-facing features (e.g., a redesigned checkout button) are rolled out via A/B tests to measure impact on conversion rates before a 100% rollout.
- **Feature Flags**: Code is merged to main and deployed frequently, hidden behind feature flags (via tools like LaunchDarkly) until the marketing or product team decides to enable them.
- **Dark Deployments**: Critical infrastructural changes (e.g., a new search indexing algorithm) run alongside the old system in production ("dark") to verify performance and accuracy before switching over.

## Bug Triaging

- **Severity Levels**: Bugs are categorized from Sev-1 (Critical outage, e.g., payment gateway down) to Sev-3 (Minor UI glitch).
- **SLA (Service Level Agreement)**: Sev-1 issues require immediate, all-hands-on-deck response. Sev-2 issues must be resolved within the current sprint.
- **Root Cause Analysis (RCA)**: Every Sev-1 incident requires a documented RCA within 48 hours to ensure the underlying systemic issue is addressed permanently.
