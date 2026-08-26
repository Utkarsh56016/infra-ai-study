---
last_mapped_commit: 798de18a326e179f27a289fe0f1c786a04380007
---

# Architecture

**Analysis Date:** 2026-08-26

## Summary

This repository is architected as a persistent study record and workflow-controlled implementation workspace. Its main behavior is procedural rather than executable: tracked documents define what to study, how to validate learning, where evidence belongs, and when Codex may perform GSD-governed build work.

## Architectural Style

- Documentation-first repository with Markdown as the system of record.
- Roadmap-driven learning architecture organized by day.
- Evidence-first progress tracking through `PROGRESS.md` and day READMEs.
- Repository-local agent governance through `AGENTS.md`.
- GSD-controlled implementation workflow through project config and future `.planning/` artifacts.

## Primary Control Flow

Study work follows the loop documented in `README.md`, `AGENTS.md`, and `project-config/01_STUDY_OPERATING_SYSTEM.md`:

```text
Understand -> Visualize -> Build -> Break -> Debug -> Explain -> Recall
```

Codex build work follows the GSD loop documented in `AGENTS.md` and `project-config/07_GSD_CODEX_WORKFLOW.md`:

```text
Discuss -> Plan -> Execute -> Verify -> Ship
```

These loops are deliberately separate. GSD verification can validate implementation work, but it does not by itself mark study understanding complete.

## Main Data Flow

The repository stores learning state as Markdown:

```text
project-config/*.md
  -> agent/session behavior
roadmap/LFX_10_DAY_ROADMAP.md
  -> planned study sequence
PROGRESS.md
  -> current day and progress log
days/day-XX-*/README.md
  -> day evidence, labs, debugging, teach-back, quiz, exit criteria
labs/, diagrams/, runbooks/, cheatsheets/, source-maps/, interview-notes/
  -> larger standalone artifacts
```

## Entry Points

- `AGENTS.md` is the agent entrypoint and should be read before decisions or implementation.
- `README.md` is the human-facing overview.
- `PROGRESS.md` is the current progress source.
- `roadmap/LFX_10_DAY_ROADMAP.md` defines the 10-day LFX ramp.
- `days/day-01-kubernetes-mental-model/README.md` is the active day file because `PROGRESS.md` says Day 1 is current and not started.

## Governance Boundaries

- Study progress must be supported by observed evidence or explicit user-provided results.
- Roadmap day completion cannot be inferred from explanations or generated code.
- Non-trivial implementation tasks must use GSD Core.
- `.planning/` is GSD implementation state, not study-completion evidence.
- Existing local changes must not be overwritten blindly.

## Current Repository State

- The tracked repository contains documentation and empty artifact directories.
- All ten `days/day-XX-*/README.md` files are scaffolded with the same evidence-oriented structure.
- `PROGRESS.md` shows Day 1 / Kubernetes Mental Model / Not started.
- No executable lab code, manifests, diagrams, runbooks, source maps, or interview notes are currently tracked.
- `infra-ai-study.zip` is tracked in the root and may be a packaged copy or external artifact.

## Future Architecture Evolution

The roadmap implies future directories will become populated:

- `labs/` with runnable experiments.
- `diagrams/` with control-flow and system diagrams.
- `runbooks/` with debugging procedures.
- `cheatsheets/` with compact reference material.
- `source-maps/` with HAMi, Volcano, Kubernetes, or runtime source maps.
- `interview-notes/` with role-specific Q&A and project defense notes.

## Critical Abstractions

- **Current day:** resolved from `PROGRESS.md`, not memory.
- **Study artifact:** a concrete repository record such as a lab, diagram, runbook, or source map.
- **Observed evidence:** real command/test/output supplied or inspected.
- **GSD phase:** an implementation control unit, separate from study day completion.
- **Source mirror:** project-config files that mirror or define ChatGPT project behavior.

*Codebase architecture analysis: 2026-08-26*
<!-- refreshed: 2026-08-26 -->
