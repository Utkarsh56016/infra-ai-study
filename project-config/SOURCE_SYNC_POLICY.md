# Project Source Synchronization Policy

## Goal

Prevent semantic drift between the ChatGPT Project source files, the GitHub repository `Utkarsh56016/infra-ai-study`, and a local checkout used by Codex.

## Canonical rule

GitHub is the persistent engineering source of truth for study progress, validated evidence, day state, labs, artifacts, and the current roadmap used for continuation.

The ChatGPT Project source files are configuration/reference mirrors used to initialize and guide the workspace.

A local checkout used by Codex is an execution workspace and should be synchronized from GitHub before starting new work.

If a Project source file and GitHub disagree, use the latest verified GitHub version until the Project source mirror is refreshed.

If a local checkout and GitHub disagree, inspect uncommitted/local work first; do not overwrite it blindly. Reconcile intentionally, then restore a clean synchronized state.

## Source mapping

| Project source | GitHub canonical/mirror path |
|---|---|
| `00_PROJECT_CONTEXT.md` | `project-config/00_PROJECT_CONTEXT.md` |
| `01_STUDY_OPERATING_SYSTEM.md` | `project-config/01_STUDY_OPERATING_SYSTEM.md` |
| `02_LFX_10_DAY_ROADMAP.md` | `roadmap/LFX_10_DAY_ROADMAP.md` |
| `03_JOB_TARGET_SKILL_MATRIX.md` | `project-config/03_JOB_TARGET_SKILL_MATRIX.md` |
| `04_PROJECT_CUSTOM_INSTRUCTIONS.md` | `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md` |
| `05_SOURCE_INDEX.md` | `project-config/05_SOURCE_INDEX.md` |
| `06_GITHUB_STUDY_WORKFLOW.md` | `project-config/06_GITHUB_STUDY_WORKFLOW.md` |
| `GSD_README.md` | `project-config/GSD_README.md` |

Additional repository-local control files:

- `AGENTS.md` — Codex entrypoint and repository operating contract.
- `project-config/07_GSD_CODEX_WORKFLOW.md` — project-specific GSD integration rules.

## Update protocol

When a shared source/config document changes:

1. Read the latest GitHub copy before writing.
2. Apply the smallest intentional change.
3. Keep the Project source and mapped GitHub document semantically identical where both are maintained.
4. Do not alter study-completion state as part of a configuration sync.
5. If only one side can be updated in the current session, GitHub remains authoritative and the other side is considered a pending mirror refresh.
6. Before resuming study after a long gap, read `README.md`, `PROGRESS.md`, the current day README, and the roadmap from GitHub.
7. Before Codex build work, synchronize the local checkout and let Codex read root `AGENTS.md`.
8. For non-trivial Codex implementation work, use GSD Core rather than ad-hoc free-form building.

## Local checkout synchronization

Before starting a new Codex session on an otherwise clean checkout:

```bash
git status --short
git pull --ff-only
```

If `git status --short` shows local changes, inspect them first. Do not pull/overwrite blindly.

After synchronization, Codex should read `AGENTS.md` and the files it references before implementation.

GSD must be installed/onboarded through its own runtime-aware installer. Do not create fake `.planning/` state or manually copy GSD runtime internals into the repository.

## Progress data is not mirrored into Project source

Dynamic evidence belongs only in GitHub/local Git history:

- completed labs
- terminal output
- quiz results
- teach-backs
- confidence scores
- debugging conclusions
- day completion state
- generated artifacts
- GSD execution/verification evidence associated with real implementation work

These should not be copied into static Project source files merely to keep them visually identical.

## Principle

Project source defines how we work.

GitHub records what actually happened.

The local Codex checkout executes against that record.
