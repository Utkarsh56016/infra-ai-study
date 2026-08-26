# Infra & AI Study

Personal engineering study log focused on GPU infrastructure, Kubernetes, Linux internals, container runtimes, MLOps, and cloud-native systems.

## Current objective

Immediate preparation for CNCF/LFX work around:

- HAMi GPU Observability
- HAMi GPU Memory Isolation
- Volcano xPU Topology-Aware Scheduling

Long-term target roles:

- AI / GPU Infrastructure Engineer
- MLOps Engineer
- Platform Engineer
- Kubernetes / Cloud-Native Engineer
- Backend AI Engineer

## Core stack

```text
Kubernetes
  ↓
scheduler / kubelet / CRI
  ↓
containerd / runc / OCI
  ↓
Linux processes / namespaces / cgroups
  ↓
NVIDIA runtime / driver / NVML / CUDA
  ↓
GPU
  ↓
HAMi / Volcano
```

## Study method

Every substantial topic follows:

```text
Understand → Visualize → Build → Break → Debug → Explain → Recall
```

Debugging uses:

```text
Symptom → Scope → Evidence → Layer → Hypothesis → Test → Conclusion
```

Conclusions are separated into:

- Observation
- Inference
- Hypothesis
- Unknown

## Codex build workflow

Repository-local Codex context starts at `AGENTS.md`.

For non-trivial implementation/build tasks, this project uses **GSD Core**:

```text
Discuss → Plan → Execute → Verify → Ship
```

The study loop and GSD loop are separate gates: GSD verifies the implementation; study completion verifies understanding, debugging ability, teach-back, quiz performance, and roadmap exit criteria.

See:

- `AGENTS.md`
- `project-config/07_GSD_CODEX_WORKFLOW.md`
- `project-config/GSD_README.md`

## Progress

| Day | Topic | Status | Artifact |
|---|---|---|---|
| 1 | Kubernetes Mental Model | In progress | — |
| 2 | Container Runtime Path | Not started | — |
| 3 | Linux Process Internals | Not started | — |
| 4 | NVIDIA GPU Stack | Not started | — |
| 5 | Kubernetes GPU Resource Model | Not started | — |
| 6 | HAMi Observability | Not started | — |
| 7 | HAMi Memory Isolation | Not started | — |
| 8 | Volcano Topology-Aware Scheduling | Not started | — |
| 9 | Go, C/C++, Upstream Code | Not started | — |
| 10 | Full-Stack Integration | Not started | — |

## Repository layout

```text
infra-ai-study/
├── AGENTS.md
├── README.md
├── PROGRESS.md
├── roadmap/
│   └── LFX_10_DAY_ROADMAP.md
├── project-config/
│   ├── 00_PROJECT_CONTEXT.md
│   ├── 01_STUDY_OPERATING_SYSTEM.md
│   ├── 03_JOB_TARGET_SKILL_MATRIX.md
│   ├── 04_PROJECT_CUSTOM_INSTRUCTIONS.md
│   ├── 05_SOURCE_INDEX.md
│   ├── 06_GITHUB_STUDY_WORKFLOW.md
│   ├── 07_GSD_CODEX_WORKFLOW.md
│   ├── GSD_README.md
│   └── SOURCE_SYNC_POLICY.md
├── days/
│   ├── day-01-kubernetes-mental-model/
│   ├── day-02-container-runtime-path/
│   └── ...
├── labs/
├── diagrams/
├── runbooks/
├── cheatsheets/
├── interview-notes/
└── source-maps/
```

Each study-day directory contains its own README with notes, lab evidence, debugging exercises, teach-back notes, quiz results, and exit criteria.
