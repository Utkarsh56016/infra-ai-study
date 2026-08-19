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

## Progress

| Day | Topic | Status | Artifact |
|---|---|---|---|
| 1 | Kubernetes Mental Model | Not started | — |
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
├── README.md
├── PROGRESS.md
├── roadmap/
│   └── LFX_10_DAY_ROADMAP.md
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
