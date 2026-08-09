# Architecture

## Role of this repository

The Aggressive Lures Design System is a shared technical and design contract. It should make independently built Aggressive Lures experiences feel related without forcing every product into one codebase.

## System boundaries

### This repository owns

- approved design tokens
- reusable interface components
- reusable interaction and content patterns
- accessibility and responsive behavior guidance
- design-system prototypes
- implementation documentation
- change history for shared UI contracts

### This repository does not own

- WordPress content or database records
- lake, guide, marina, fishing-report, or weather business logic
- secrets, credentials, API keys, or production configuration
- company-wide strategy and institutional knowledge better maintained in Notion
- deployable application code unless a future architectural decision deliberately changes this boundary

## Layered model

1. **Knowledge and decisions** — Notion
2. **Shared design contract** — this repository
3. **Product implementation** — product or plugin repositories
4. **Deployment/runtime** — hosting, WordPress, APIs, and infrastructure
5. **Field feedback and intelligence** — real-world usage, fishing reports, analytics, and research feeding improvements back into the earlier layers

## Growth rule

Start with one repository where a shared design system is useful. Create additional repositories when an artifact has an independent lifecycle, deployment target, permission boundary, or release process. Do not split repositories merely because a folder could become a repository.

Likely future repository candidates may include the fishing conditions experience and mature custom WordPress plugins. These are candidates, not commitments.

## AI collaborator model

AI collaborators may research, propose, implement, test, document, and review. Architectural decisions that materially affect brand, production behavior, data handling, security, or system boundaries should remain visible to human review.

Preferred workflow:

1. Capture the problem and relevant context.
2. Define the smallest useful change.
3. Work on a branch rather than directly on `main`.
4. Validate the change.
5. Open a pull request that explains what changed and why.
6. Review before merge.
7. Record durable business or architectural decisions in the appropriate knowledge system.

## Architecture decision records

As technical choices become consequential, add short Architecture Decision Records (ADRs) under `docs/decisions/`. An ADR should explain context, decision, alternatives, consequences, and status. We should not create ADRs for trivial implementation details.

## Design-system maturity stages

### Stage 0 — Foundation
Governance, boundaries, vocabulary, contribution workflow.

### Stage 1 — Tokens
Approved color, typography, spacing, radius, elevation, motion, and responsive primitives. Tokens should not be invented before brand decisions are approved.

### Stage 2 — Core components
Buttons, links, inputs, cards, alerts, navigation, data-display primitives, and accessibility states.

### Stage 3 — Fishing patterns
Conditions cards, pressure/trend visualization patterns, lake information, guide/marina profiles, report summaries, trust indicators, and field-oriented mobile interactions.

### Stage 4 — Distribution
Package or otherwise expose stable design-system artifacts to product repositories when the maintenance benefit exceeds the added tooling cost.

## Review triggers

Revisit this architecture when any of these become true:

- multiple applications duplicate the same components
- shared tokens are being copied manually between projects
- release coordination becomes painful
- a component library needs automated packaging/versioning
- external contributors begin working in the repositories
- production security or compliance requirements increase
- a product requires a technology stack incompatible with the current shared implementation
