# Aggressive Lures Design System

Shared design and interface foundation for Aggressive Lures digital products.

## Purpose

This repository exists to keep reusable design decisions, interface patterns, tokens, components, prototypes, and implementation guidance consistent across the Aggressive Lures ecosystem.

It is intentionally **not** the repository for the entire AggressiveLures.com website. Product-specific applications and WordPress plugins can live in their own repositories as they mature while consuming or referencing this shared foundation.

## Working principles

- Trust before novelty.
- Build what is real. Do not create empty architecture merely to look complete.
- Mobile and field use matter. Anglers may be using these interfaces outdoors, on docks, in boats, and on phones.
- Accessibility and legibility are product requirements.
- Unknown values stay unknown rather than being invented.
- Reusable patterns belong here; product-specific business logic belongs with the product.
- Human approval remains part of meaningful architectural and production decisions.

## Repository map

- `docs/` — architecture, governance, and implementation guidance
- `tokens/` — shared visual design tokens as they become approved
- `components/` — reusable UI components when implementation begins
- `patterns/` — larger reusable interaction and content patterns
- `assets/` — approved shared design assets
- `prototypes/` — experiments that are not production contracts
- `.github/` — contribution and pull request workflow support

Directories should be created when they contain something useful. Empty folders are intentionally avoided.

## Current phase

Foundation. The first goal is to establish how humans and AI collaborators safely design, document, review, and evolve the system before production components accumulate.

## Relationship to other systems

Notion holds broader company knowledge, decisions, research, and operating context. GitHub holds versioned technical artifacts and their change history. Product repositories hold deployable product-specific code. This repository provides the shared design-system layer between strategy and implementation.
