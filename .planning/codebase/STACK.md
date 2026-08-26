---
last_mapped_commit: 798de18a326e179f27a289fe0f1c786a04380007
---

# Technology Stack

**Analysis Date:** 2026-08-26

## Summary

This repository is a Markdown-first engineering study workspace, not a runnable application codebase. Its primary "stack" is Git-tracked documentation, study-day templates, GSD Core workflow guidance, and repository-local agent instructions.

## Languages And File Types

- Markdown is the dominant authored format: `README.md`, `PROGRESS.md`, `AGENTS.md`, `CONTRIBUTING.md`, `roadmap/LFX_10_DAY_ROADMAP.md`, and all `project-config/*.md` files.
- Study-day content lives in Markdown templates under `days/day-XX-*/README.md`.
- No first-party Python, Go, C, C++, JavaScript, TypeScript, YAML manifests, or shell scripts are currently tracked as project artifacts.
- `infra-ai-study.zip` is tracked at the repository root as a binary archive artifact.
- `.gitignore` is tracked, but application dependency manifests are absent.

## Runtime And Tooling

- Git is the durable state mechanism for the study record and future GSD artifacts.
- GSD Core is installed locally under `.agents/` in the working tree, but `.agents/` is currently untracked.
- Repository-local Codex behavior is defined by `AGENTS.md`.
- GSD/Codex workflow policy is documented in `project-config/07_GSD_CODEX_WORKFLOW.md`.
- The supplied GSD reference copied into project context is `project-config/GSD_README.md`.

## Application Dependencies

No application dependency files were found:

- No `package.json`
- No `go.mod`
- No `requirements.txt`, `pyproject.toml`, or `Pipfile`
- No `Cargo.toml`
- No `Dockerfile`
- No Kubernetes manifests

This means there is currently no build graph, package manager, runtime service, or executable entrypoint to map.

## Domain Stack

The study domain stack is explicitly documented in `README.md`, `AGENTS.md`, `project-config/00_PROJECT_CONTEXT.md`, and `roadmap/LFX_10_DAY_ROADMAP.md`:

```text
Kubernetes -> scheduler / kubelet / CRI -> containerd / runc / OCI
-> Linux processes / namespaces / cgroups
-> NVIDIA runtime / driver / NVML / CUDA
-> GPU -> HAMi -> Volcano
```

## Configuration Sources

- `AGENTS.md` is the repository-local operating contract for Codex.
- `project-config/00_PROJECT_CONTEXT.md` records background, goals, LFX applications, and prior experience.
- `project-config/01_STUDY_OPERATING_SYSTEM.md` defines the learning loop and study session structure.
- `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md` is the canonical project instruction text.
- `project-config/05_SOURCE_INDEX.md` maps project-source files to repository paths.
- `project-config/06_GITHUB_STUDY_WORKFLOW.md` defines evidence and progress rules.
- `project-config/SOURCE_SYNC_POLICY.md` defines source-of-truth and sync behavior.

## State Trackers

- `README.md` provides the public overview and repository layout.
- `PROGRESS.md` is the current study progress source. It currently records Day 1 as not started.
- `roadmap/LFX_10_DAY_ROADMAP.md` is the semantic 10-day study roadmap.
- `days/day-01-kubernetes-mental-model/README.md` through `days/day-10-integration/README.md` are day-level templates and future evidence records.

## Tooling Implications

- Build/test commands are not meaningful yet because there is no executable implementation.
- Future non-trivial code labs should use GSD Core before broad implementation, per `AGENTS.md` and `project-config/07_GSD_CODEX_WORKFLOW.md`.
- Study completion must be validated separately from GSD implementation completion.

*Codebase stack analysis: 2026-08-26*
<!-- refreshed: 2026-08-26 -->
