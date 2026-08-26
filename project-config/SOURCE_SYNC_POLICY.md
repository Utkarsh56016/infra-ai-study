# Project Source Synchronization Policy

## Goal

Prevent semantic drift between the ChatGPT Project source files and the GitHub repository `Utkarsh56016/infra-ai-study`.

## Canonical rule

GitHub is the persistent engineering source of truth for study progress, validated evidence, day state, labs, artifacts, and the current roadmap used for continuation.

The ChatGPT Project source files are configuration/reference mirrors used to initialize and guide the workspace.

If a Project source file and GitHub disagree, use the latest verified GitHub version until the Project source mirror is refreshed.

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

## Update protocol

When a shared source/config document changes:

1. Read the latest GitHub copy before writing.
2. Apply the smallest intentional change.
3. Keep the Project source and mapped GitHub document semantically identical.
4. Do not alter study-completion state as part of a configuration sync.
5. If only one side can be updated in the current session, GitHub remains authoritative and the other side is considered a pending mirror refresh.
6. Before resuming study after a long gap, read `README.md`, `PROGRESS.md`, the current day README, and the roadmap from GitHub.

## Progress data is not mirrored into Project source

Dynamic evidence belongs only in GitHub:

- completed labs
- terminal output
- quiz results
- teach-backs
- confidence scores
- debugging conclusions
- day completion state
- generated artifacts

These should not be copied into static Project source files.

## Principle

Project source defines how we work.

GitHub records what actually happened.
