# Contribution Workflow

This workflow is deliberately lightweight. Its purpose is to make changes understandable and reversible, not to add ceremony.

## Core rule

Do not make meaningful shared-system changes directly on `main`.

## Standard flow

1. Start from the current `main` branch.
2. Create a focused branch.
3. Make the smallest coherent set of changes.
4. Review the diff for accidental or unrelated edits.
5. Run relevant validation.
6. Commit with a short description of the change.
7. Open a draft pull request.
8. Explain what changed, why it changed, impact, and validation.
9. Resolve questions or requested changes.
10. Merge after human approval when the change is ready.

## Branch naming

AI-assisted branches should use:

`agent/<short-description>`

Examples:

- `agent/initial-repository-foundation`
- `agent/add-color-tokens`
- `agent/conditions-card-pattern`

Other contributors can use an equivalent descriptive convention as the team grows.

## Commit guidance

A commit should describe one understandable step. Prefer messages such as:

- `Add repository foundation`
- `Document responsive breakpoints`
- `Add conditions card accessibility states`

Avoid vague messages such as `updates`, `stuff`, or `fix`.

## Pull request expectations

A useful pull request answers:

- What changed?
- Why is the change needed?
- What does it affect?
- How was it validated?
- Is anything intentionally deferred?

Draft pull requests are encouraged while a change is still being explored.

## AI collaboration rules

AI-generated work is not exempt from review. AI collaborators should:

- distinguish facts from proposals
- avoid inventing brand standards, data, APIs, or requirements
- preserve explicit unknowns
- keep changes scoped
- document important assumptions
- flag security, privacy, accessibility, and architectural consequences
- prefer reversible changes during exploration
- never commit credentials, secrets, tokens, private customer data, or private fishing-location information

## Definition of done

The definition depends on the change, but a shared design-system change is generally done when:

- the intended behavior is documented
- implementation and documentation agree
- relevant accessibility states are considered
- mobile behavior is considered
- validation has been performed
- the pull request explains the change
- human review has occurred for meaningful shared-system decisions

## When this workflow should grow

Add automation only when it removes a real recurring problem. Possible future additions include formatting checks, linting, accessibility tests, visual regression tests, automated builds, release notes, package publishing, and branch protection.
