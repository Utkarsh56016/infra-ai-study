---
last_mapped_commit: 798de18a326e179f27a289fe0f1c786a04380007
---

# Structure

**Analysis Date:** 2026-08-26

## Summary

The repository structure is organized around learning records: root-level orientation, project configuration, a 10-day roadmap, per-day evidence templates, and dedicated artifact directories for labs, diagrams, runbooks, cheat sheets, interview notes, and source maps.

## Top-Level Layout

```text
.
├── AGENTS.md
├── CONTRIBUTING.md
├── PROGRESS.md
├── README.md
├── infra-ai-study.zip
├── roadmap/
├── project-config/
├── days/
├── labs/
├── diagrams/
├── runbooks/
├── cheatsheets/
├── interview-notes/
└── source-maps/
```

## Root Files

- `AGENTS.md` defines repository-specific agent instructions, GSD setup rules, evidence boundaries, and modification rules.
- `README.md` introduces the study workspace, goals, stack, progress table, and intended layout.
- `PROGRESS.md` stores the current day, topic, status, progress log, and skill gaps.
- `CONTRIBUTING.md` defines commit-message style for study evidence.
- `.gitignore` is tracked but was not expanded during this mapping.
- `infra-ai-study.zip` is a tracked binary archive at the root.

## Roadmap

- `roadmap/LFX_10_DAY_ROADMAP.md` defines Days 1 through 10.
- Each roadmap day has topics, output expectations, and exit tests.
- The roadmap begins with Kubernetes fundamentals and moves down through runtime/Linux/GPU internals, then back up into HAMi and Volcano.

## Project Configuration

- `project-config/00_PROJECT_CONTEXT.md` captures background, LFX context, prior internship experience, and portfolio context.
- `project-config/01_STUDY_OPERATING_SYSTEM.md` defines the default teaching/study session format.
- `project-config/03_JOB_TARGET_SKILL_MATRIX.md` maps target roles to skill requirements.
- `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md` is the canonical instruction document.
- `project-config/05_SOURCE_INDEX.md` maps project source files to repository paths.
- `project-config/06_GITHUB_STUDY_WORKFLOW.md` defines the GitHub evidence workflow.
- `project-config/07_GSD_CODEX_WORKFLOW.md` defines how GSD and Codex fit this repo.
- `project-config/GSD_README.md` is a local reference for GSD Core.
- `project-config/SOURCE_SYNC_POLICY.md` defines synchronization and source-of-truth policy.

## Day Directories

Each day directory has a `README.md` with sections for status, orientation, mental model, mechanism, lab, break/debug scenario, teach-back, quiz, exit criteria, and artifacts.

- `days/day-01-kubernetes-mental-model/README.md`
- `days/day-02-container-runtime-path/README.md`
- `days/day-03-linux-process-internals/README.md`
- `days/day-04-nvidia-gpu-stack/README.md`
- `days/day-05-kubernetes-gpu-resource-model/README.md`
- `days/day-06-hami-observability/README.md`
- `days/day-07-hami-memory-isolation/README.md`
- `days/day-08-volcano-topology-aware-scheduling/README.md`
- `days/day-09-go-cpp-upstream/README.md`
- `days/day-10-integration/README.md`

## Artifact Directories

The following directories exist for future substantial artifacts:

- `labs/`
- `diagrams/`
- `runbooks/`
- `cheatsheets/`
- `interview-notes/`
- `source-maps/`

At mapping time, these directories are present but have no tracked files.

## Naming Conventions

- Study days use `day-XX-topic-name`.
- Project config files use numeric prefixes to preserve ordering.
- Roadmap file uses an explicit scope name: `LFX_10_DAY_ROADMAP.md`.
- Markdown headings follow clear topic-oriented titles.

## Important Generated/Local Directories

- `.agents/` exists locally and contains GSD/agent runtime material, but it is untracked.
- `.opencode/` exists locally and is untracked.
- `.planning/codebase/` is being created by this workflow as GSD codebase map output.

*Codebase structure analysis: 2026-08-26*
<!-- refreshed: 2026-08-26 -->
