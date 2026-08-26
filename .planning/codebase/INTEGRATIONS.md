---
last_mapped_commit: 798de18a326e179f27a289fe0f1c786a04380007
---

# Integrations

**Analysis Date:** 2026-08-26

## Summary

The repository has no executable service integrations yet. The meaningful integrations are workflow and source-of-truth integrations: GitHub as the durable study record, Codex as the local coding agent, and GSD Core as the required framework for non-trivial implementation work.

## External Services

No code-level integrations were found for:

- Databases
- Cloud APIs
- Authentication providers
- Webhooks
- Message queues
- Observability backends
- Payment or SaaS APIs

There are no config files or source files containing calls to external services.

## Repository And GitHub

- `project-config/06_GITHUB_STUDY_WORKFLOW.md` identifies `Utkarsh56016/infra-ai-study` as the persistent engineering notebook and progress tracker.
- `project-config/SOURCE_SYNC_POLICY.md` states that GitHub is authoritative for validated study progress, evidence, day state, labs, and artifacts.
- `README.md` and `PROGRESS.md` are the primary tracker files used for resume decisions.
- `CONTRIBUTING.md` defines commit-message examples for learning evidence.

## Codex And Agent Workflow

- `AGENTS.md` is the root agent instruction file for this repository.
- `project-config/07_GSD_CODEX_WORKFLOW.md` requires GSD Core for non-trivial Codex build work.
- `.agents/` exists in the local working tree and contains GSD runtime files and skills, but it is currently untracked.
- `.opencode/` also exists as an untracked local runtime/config directory.

## GSD Core

- `project-config/GSD_README.md` documents GSD Core as a context-engineering and spec-driven development framework.
- The project-specific rule in `project-config/07_GSD_CODEX_WORKFLOW.md` separates the GSD loop from study completion.
- Non-trivial build work should move through Discuss, Plan, Execute, Verify, and Ship.
- GSD planning artifacts belong under `.planning/` once onboarding and project initialization proceed.

## Study Platform Assumptions

`project-config/01_STUDY_OPERATING_SYSTEM.md` and `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md` name the intended local lab environment:

- Arch Linux
- HP Victus 15
- Ryzen 5 5600H
- RTX 3050 4 GB
- 16 GB RAM
- Preferred tools include kind, Docker/containerd, Linux namespaces, cgroups v2, `/proc`, systemd, small Python/Go/C programs, and mock Kubernetes resources.

These are study assumptions, not checked executable dependencies in this repo.

## Future Integration Hotspots

Likely future integrations are implied by the roadmap:

- Kubernetes API and scheduler/kubelet behavior in Days 1, 5, and 8.
- containerd/runc/OCI runtime behavior in Day 2.
- Linux process, namespace, and cgroup interfaces in Day 3.
- NVIDIA driver, CUDA, NVML, NVIDIA Container Toolkit, and DCGM in Days 4, 6, and 7.
- HAMi and Volcano upstream source trees in Days 6 through 9.

## Secret Handling

No explicit secrets-management integration exists. Generated docs should avoid copying credentials or command output that includes tokens. The repository policy already requires separating observed evidence from examples and avoiding fabricated terminal output.

*Codebase integrations analysis: 2026-08-26*
<!-- refreshed: 2026-08-26 -->
