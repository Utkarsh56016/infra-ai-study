# AGENTS.md — Infra & AI Study

## Repository purpose

This repository is Utkarsh Mishra's persistent engineering study record for GPU/AI infrastructure, Kubernetes, Linux internals, container runtimes, MLOps, cloud-native systems, production debugging, and LFX/CNCF preparation.

The immediate LFX focus is:

- HAMi — GPU Observability: Metrics and Dashboards
- HAMi — Fix GPU Memory Isolation for Child and SSH Processes
- Volcano — Generic xPU Topology-Aware Scheduling

Shared technical path:

```text
Kubernetes → scheduler / kubelet / CRI → containerd / runc / OCI
→ Linux processes / namespaces / cgroups
→ NVIDIA runtime / driver / NVML / CUDA
→ GPU → HAMi → Volcano
```

## Read this first

Before making decisions about current progress or implementation, read:

1. `README.md`
2. `PROGRESS.md`
3. `roadmap/LFX_10_DAY_ROADMAP.md`
4. the current `days/day-XX-*/README.md`
5. `project-config/00_PROJECT_CONTEXT.md`
6. `project-config/01_STUDY_OPERATING_SYSTEM.md`
7. `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md`
8. `project-config/06_GITHUB_STUDY_WORKFLOW.md`
9. `project-config/07_GSD_CODEX_WORKFLOW.md`

GitHub repository state is authoritative for dynamic progress and evidence.

## Two operating loops

### Study / learning work

Use:

```text
Understand → Visualize → Build → Break → Debug → Explain → Recall
```

A study topic is not complete until its exit criteria are genuinely satisfied. Do not invent terminal output, test results, quiz results, teach-backs, confidence, or completion state.

### Codex build / implementation work

All non-trivial Codex building tasks must use GSD Core.

Use the GSD phase loop:

```text
Discuss → Plan → Execute → Verify → Ship
```

This applies to implementation work such as:

- multi-file lab code
- tooling or automation
- Go/C/Python implementations
- Kubernetes operators/controllers/plugins
- scheduler/runtime experiments
- substantial refactors
- reusable utilities
- production-style project work

Do not bypass GSD by jumping directly from an idea to broad code edits.

Small read-only investigations, quizzes, explanations, and trivial documentation corrections do not require a GSD phase unless explicitly requested.

## GSD setup rule

GSD Core must be installed through its installer for the selected runtime. Do not manually copy framework files from another runtime.

For this existing repository, if GSD has not yet been initialized locally:

1. install GSD Core using its installer and choose Codex + local project installation;
2. onboard this existing repository with `/gsd-onboard`;
3. use the generated `.planning/` artifacts as GSD's persistent implementation state.

Do not fabricate `.planning/STATE.md`, phase completion, verification output, or shipped work.

See `project-config/GSD_README.md` and `project-config/07_GSD_CODEX_WORKFLOW.md`.

## Evidence boundary

For study labs and implementation verification, distinguish:

- **Observed** — supplied by a real command, test, experiment, or inspected source
- **Expected** — healthy/reference behavior
- **Inference** — conclusion supported by observations
- **Hypothesis** — plausible but unverified
- **Unknown** — unresolved

## Modification rules

- Inspect existing architecture/files before changing them.
- Prefer the smallest testable change.
- Preserve existing content and directory structure unless restructuring is intentional.
- Read an existing tracked file before replacing it.
- Never mark a roadmap day complete because code was merely written.
- GSD verification and study exit criteria are separate gates; satisfy whichever applies to the task.
- Update `PROGRESS.md` and a day README only after validated study milestones.
- Keep substantial artifacts in dedicated directories (`labs/`, `diagrams/`, `runbooks/`, `source-maps/`, etc.).

## Current starting state

At repository initialization, Day 1 is the current roadmap day and is not complete. Always re-read `PROGRESS.md` rather than assuming this remains true.
