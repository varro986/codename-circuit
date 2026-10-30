# Circuit

An integration and user interface platform for small and medium businesses.

## Goal

Give a small or medium business one layer on top of the systems it already has, so it can automate its processes and
get the screens it needs for each use case, without replacing what is already there.

## Description

Circuit has two halves:

- **Interfaces built for the use case**: graphical interfaces (JSX components) made for a specific need and plugged
  into the platform.
- **Integration**: connectors to many external APIs and to the systems already in the company, so interfaces and
  automations work on real data.

Everything is meant to be fully auditable and compliant: every action leaves a trace, and the product must be usable
by a business that has to answer for what its automations do.

## Technologies

To be decided (see "To do"). Interfaces in JSX (React or a compatible library); the rest must run on Windows and
Linux, with open source dependencies (MIT or Apache 2.0 preferred).

## Dependencies

None yet. Nothing depends on Circuit.

## Architecture

```
codename-circuit/
|-- README.md         what the project is
|-- AGENTS.md         rules for coding assistants: common rules, then the product's own
|-- CLAUDE.md         shell for Claude Code (@AGENTS.md)
|-- CONTRIBUTING.md   how to contribute (specs first, dev then main)
|-- LICENSE           MIT
|-- SECURITY.md       how to report a vulnerability
|-- CODE_OF_CONDUCT.md
|-- specs/            brainstorming.md; architecture as it comes
|   |-- features/     one folder per feature: spec.md, plan.md with its tasks
|   \-- decisions/    ADRs
|-- src/              source code
|-- tests/            tests, from the acceptance criteria
|-- tools/            deterministic tools for agents and people
|-- .githooks/        pre-commit: gitleaks on staged files
|-- .github/          CI (gitleaks), issue and PR templates, Dependabot
|-- .gitleaks.toml    secret scan rules
|-- .gitignore
\-- .editorconfig     shared editor settings
```

## Rules

- **Auditable by design**: every automation and integration call is logged with who, what and when.
- **On top, not instead**: Circuit integrates the systems a business already uses; it does not replace them.

