# Infra AI Study Workspace

## What This Is

This is a durable engineering study and implementation workspace for AI/GPU infrastructure, Kubernetes, Linux internals, container runtimes, MLOps, and CNCF/LFX preparation. It guides and records practical learning through real labs, debugging exercises, source-code reading, diagrams, runbooks, and implementation artifacts.

This is not a normal greenfield application. GSD manages non-trivial implementation/build work inside the repository, while the existing study roadmap and progress files remain the source of truth for validated learning progress.

## Core Value

The repository must demonstrate real, evidence-backed ability to operate, debug, implement, and design AI/GPU infrastructure systems without fabricating progress or replacing the study workflow.

## Requirements

### Validated

- ✓ Repository has a canonical LFX study roadmap in `roadmap/LFX_10_DAY_ROADMAP.md` — existing
- ✓ Repository tracks current study progress in `PROGRESS.md` — existing
- ✓ Repository has day-level evidence templates in `days/day-01-kubernetes-mental-model/README.md` through `days/day-10-integration/README.md` — existing
- ✓ Repository has project operating instructions in `AGENTS.md` and `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md` — existing
- ✓ Repository separates study workflow from Codex/GSD implementation workflow in `project-config/07_GSD_CODEX_WORKFLOW.md` — existing
- ✓ Repository has dedicated artifact directories for labs, diagrams, runbooks, cheat sheets, interview notes, and source maps — existing
- ✓ Codebase map exists in `.planning/codebase/` — existing

### Active

- [ ] Initialize GSD planning state for implementation/build work without replacing the study roadmap.
- [ ] Define requirements that protect the boundary between learning progress and implementation progress.
- [ ] Create a GSD roadmap for repository infrastructure and implementation artifacts.
- [ ] Ensure future non-trivial labs and infrastructure prototypes use Discuss -> Plan -> Execute -> Verify -> Ship.
- [ ] Preserve evidence discipline: no fabricated command output, tests, benchmarks, root causes, confidence, or completion.
- [ ] Keep `PROGRESS.md` and `days/*` updates tied to validated study evidence only.

### Out of Scope

- Replacing `roadmap/LFX_10_DAY_ROADMAP.md` with a GSD roadmap — the roadmap is the learning curriculum.
- Marking study topics or days complete through GSD initialization — study completion has separate exit criteria.
- Creating fake lab output, test results, benchmarks, quiz results, teach-backs, or debugging conclusions — evidence must be real.
- Building a product UI or external service as the initial GSD project — this repository is a study and implementation workspace.
- Requiring expensive multi-GPU infrastructure for concepts that can be reproduced locally — the intended machine is modest and local-first.

## Context

The immediate LFX/CNCF preparation focus is:

- HAMi GPU Observability: Metrics and Dashboards
- HAMi GPU Memory Isolation for Child and SSH Processes
- Volcano Generic xPU Topology-Aware Scheduling

The shared technical path is:

```text
Kubernetes -> scheduler / kubelet / CRI -> containerd / runc / OCI
-> Linux processes / namespaces / cgroups
-> NVIDIA runtime / driver / NVML / CUDA
-> GPU -> HAMi -> Volcano
```

Study work uses:

```text
Understand -> Visualize -> Build -> Break -> Debug -> Explain -> Recall
```

Codex implementation work uses GSD:

```text
Discuss -> Plan -> Execute -> Verify -> Ship
```

The current tracked progress state is Day 1, Kubernetes Mental Model, not started. That remains unchanged by GSD initialization.

## Constraints

- **Evidence**: Record only observed command output, tests, benchmarks, and conclusions. Use expected/inference/hypothesis/unknown labels where appropriate.
- **Progress tracking**: `PROGRESS.md` and `days/*` may change only after validated study progress.
- **Workflow boundary**: `.planning/*` represents GSD implementation/build state, not study completion.
- **Roadmap boundary**: `roadmap/LFX_10_DAY_ROADMAP.md` remains the learning curriculum.
- **Local environment**: Prefer labs that work on Arch Linux, HP Victus 15, Ryzen 5 5600H, RTX 3050 4 GB, and 16 GB RAM.
- **Cost**: Avoid requiring expensive cloud or multi-GPU infrastructure when local or simulated labs can teach the same concept.
- **Implementation process**: Non-trivial multi-file labs, tools, prototypes, and reusable utilities must go through GSD phases.
- **Repository preservation**: Preserve existing layout and user changes unless restructuring is explicit.

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Keep the LFX roadmap as the study curriculum | It already defines the learning sequence and exit tests | — Pending |
| Use GSD only for non-trivial implementation/build work | Study progress and software delivery need different gates | — Pending |
| Keep `.planning/*` separate from `PROGRESS.md` and `days/*` | GSD verification does not prove learning completion | — Pending |
| Require real evidence before progress updates | The repository is meant to build defensible competence, not surface-level notes | — Pending |
| Prefer local-first labs | The target environment can reproduce many system concepts without expensive infrastructure | — Pending |

## Evolution

This document evolves at phase transitions and milestone boundaries.

**After each phase transition** (via `/gsd-transition`):
1. Requirements invalidated? -> Move to Out of Scope with reason
2. Requirements validated? -> Move to Validated with phase reference
3. New requirements emerged? -> Add to Active
4. Decisions to log? -> Add to Key Decisions
5. "What This Is" still accurate? -> Update if drifted

**After each milestone** (via `/gsd-complete-milestone`):
1. Full review of all sections
2. Core Value check -> still the right priority?
3. Audit Out of Scope -> reasons still valid?
4. Update Context with current state

---
*Last updated: 2026-08-26 after initialization*
