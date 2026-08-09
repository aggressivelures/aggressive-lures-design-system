# Growth Roadmap

This roadmap separates what is useful now from what should wait until the system earns the complexity.

## Build now

### Repository foundation
- clear purpose and boundaries
- branch and pull request workflow
- human/AI collaboration expectations
- architecture documentation

### Inventory before standardization
Before creating design tokens or components, inventory the real interfaces, WordPress patterns, prototypes, and brand decisions already in use. Reuse evidence before creating a new standard.

### First practical targets
Prioritize patterns that already have real Aggressive Lures use cases, especially mobile and fishing-intelligence experiences.

## Build when approved inputs exist

### Design tokens
Create tokens only after the underlying values are approved:

- colors
- typography
- spacing
- borders/radii
- elevation
- motion
- breakpoints

### Core components
Create reusable components when at least one real product needs them and the expected reuse is credible.

### Documentation examples
Add usage examples, accessibility notes, do/don't guidance, and responsive states as components become real.

## Build when multiple products consume the system

- automated component documentation
- package versioning
- changelog/release process
- visual regression testing
- automated accessibility checks
- CI validation
- dependency update automation
- semantic versioning if consumers require stable contracts

## Build when the team grows

- CODEOWNERS
- stronger branch protection
- contributor roles and permissions
- issue forms
- formal release approvals
- security reporting process
- automated deployment environments

## Questions that should trigger architectural review

- Are two products copying the same implementation?
- Are changes to shared UI breaking another product?
- Are humans or AI collaborators unsure which source is authoritative?
- Is a design decision duplicated between Notion and code without a clear ownership rule?
- Are releases becoming difficult to coordinate?
- Are permissions broader than contributors need?
- Is sensitive information entering source control?

## Principle

Complexity should be purchased with evidence. We add infrastructure when the cost of not having it becomes larger than the cost of maintaining it.
