---
last_mapped_commit: 798de18a326e179f27a289fe0f1c786a04380007
---

# Concerns

**Analysis Date:** 2026-08-26

## Summary

The repository is healthy as an initial study scaffold, but most learning artifacts are not populated yet. The main risks are evidence drift, premature progress updates, placeholder accumulation, binary artifact ambiguity, and the absence of automated checks once code labs begin.

## High-Signal Concerns

### Placeholder-heavy day files

All ten `days/day-XX-*/README.md` files contain `_TBD_`, `TBD`, and unchecked exit criteria. This is acceptable for initialization, but it means the repository should not be treated as evidence of completed study.

Relevant paths:

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

### Current progress is intentionally not started

`PROGRESS.md` records:

- Current day: Day 1
- Current topic: Kubernetes Mental Model
- Status: Not started

Any future update should be tied to observed lab evidence, teach-back, quiz, and exit criteria rather than explanation alone.

### No executable validation yet

There are no tests, CI workflows, scripts, manifests, or application code. Once labs are added, the repo will need lightweight validation suited to the artifact type, such as command transcripts, expected-vs-observed sections, or actual test commands for maintained code.

### Tracked binary archive

`infra-ai-study.zip` is tracked at the repository root. Its source, purpose, freshness, and relationship to the Markdown files are not documented in the visible repo files. Binary archives can drift from the source tree and make reviews harder.

### Empty artifact directories

The intended artifact directories exist but do not currently contain tracked files:

- `labs/`
- `diagrams/`
- `runbooks/`
- `cheatsheets/`
- `interview-notes/`
- `source-maps/`

This is fine for scaffolding, but future sessions should prefer adding standalone artifacts there rather than overloading day READMEs.

### GSD state is not initialized yet

Before this mapping workflow, `.planning/PROJECT.md`, `.planning/REQUIREMENTS.md`, `.planning/ROADMAP.md`, and `.planning/STATE.md` did not exist. GSD onboarding should proceed through the intended gates rather than fabricating planning state.

## Security And Evidence Risks

- No credential files were found in the tracked source list.
- Future lab outputs may accidentally contain tokens, kubeconfigs, hostnames, or cluster-specific details.
- Project policy in `project-config/06_GITHUB_STUDY_WORKFLOW.md` should be followed: record real evidence, avoid secrets, and distinguish observed output from expected examples.

## Maintainability Risks

- `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md`, `AGENTS.md`, and `project-config/07_GSD_CODEX_WORKFLOW.md` overlap in policy. This is useful for reinforcement but can drift if updated independently.
- `project-config/05_SOURCE_INDEX.md` refers to `02_LFX_10_DAY_ROADMAP.md` as a project source while the repository path is `roadmap/LFX_10_DAY_ROADMAP.md`; the mapping table resolves it correctly.
- As code labs arrive, documentation-only conventions may not be enough. The repo will need language-specific style, layout, and test guidance.

## Recommended Mitigations

- Keep `PROGRESS.md` conservative until real study evidence is recorded.
- For each study day, add at least one concrete artifact under `labs/`, `diagrams/`, `runbooks/`, `cheatsheets/`, `source-maps/`, or `interview-notes/`.
- Document or remove `infra-ai-study.zip` if it is not intentionally maintained.
- Add test/verification notes with every maintained code lab.
- When editing mirrored project-config files, use `project-config/SOURCE_SYNC_POLICY.md` to prevent semantic drift.
- After this map, rerun `/gsd-onboard` so GSD can continue to docs/project initialization.

## Current Unknowns

- Whether `infra-ai-study.zip` is meant to be a source snapshot, import artifact, or accidental tracked file.
- Whether `.agents/` and `.opencode/` should remain untracked local runtime directories.
- Which exact lab implementation will be the first maintained code artifact.

*Codebase concerns analysis: 2026-08-26*
<!-- refreshed: 2026-08-26 -->
