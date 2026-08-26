# Requirements: Infra AI Study Workspace

**Defined:** 2026-08-26
**Core Value:** The repository must demonstrate real, evidence-backed ability to operate, debug, implement, and design AI/GPU infrastructure systems without fabricating progress or replacing the study workflow.

## v1 Requirements

### Governance

- [ ] **GOV-01**: The repository preserves `roadmap/LFX_10_DAY_ROADMAP.md` as the learning curriculum and does not replace it with `.planning/ROADMAP.md`.
- [ ] **GOV-02**: GSD artifacts under `.planning/` represent implementation/build state, not validated study completion.
- [ ] **GOV-03**: Future non-trivial implementation work has a clear route through Discuss, Plan, Execute, Verify, and Ship.
- [ ] **GOV-04**: Study progress updates to `PROGRESS.md` and `days/*` require real evidence, debugging, teach-back, quiz, and exit-criteria validation.

### Evidence

- [ ] **EVID-01**: Lab and debugging artifacts distinguish Observed, Expected, Inference, Hypothesis, and Unknown.
- [ ] **EVID-02**: Repository artifacts never record fabricated command output, tests, benchmarks, root causes, confidence, or completion.
- [ ] **EVID-03**: Study-day artifacts preserve the Understand -> Visualize -> Build -> Break -> Debug -> Explain -> Recall loop.
- [ ] **EVID-04**: Substantial artifacts are stored in dedicated directories instead of overloading day READMEs.

### Labs

- [ ] **LAB-01**: Reusable lab artifacts can be added for Kubernetes, container runtime, Linux process, GPU, HAMi, and Volcano topics.
- [ ] **LAB-02**: Maintained code labs include verification commands or clearly labeled manual validation steps.
- [ ] **LAB-03**: Labs are designed for the local-first target environment unless a topic truly requires external infrastructure.
- [ ] **LAB-04**: Failure/debugging scenarios are captured alongside successful-path lab behavior.

### Source Mapping

- [ ] **SRC-01**: Source-code reading artifacts can be created for Kubernetes, containerd/runc, NVIDIA tooling, HAMi, and Volcano.
- [ ] **SRC-02**: Source maps identify entrypoints, ownership boundaries, test locations, and relevant upstream commands where known.
- [ ] **SRC-03**: Upstream-source conclusions are labeled as observed or inferred from inspected source.

### Verification

- [ ] **VER-01**: Implementation phases define concrete verification criteria before being marked complete.
- [ ] **VER-02**: GSD verification results do not automatically mark study-day exit criteria complete.
- [ ] **VER-03**: Progress/status files remain conservative when evidence is missing or incomplete.
- [ ] **VER-04**: Generated planning docs avoid leaking secrets or environment-specific sensitive details.

### Recall And Interview

- [ ] **RECALL-01**: The workspace supports teach-back, quiz, and interview-note artifacts for the target AI/GPU infrastructure roles.
- [ ] **RECALL-02**: Interview-prep artifacts are grounded in real experience and defensible repository evidence.
- [ ] **RECALL-03**: Final summaries and cheat sheets trace back to labs, diagrams, runbooks, or source maps.

## v2 Requirements

### Automation

- **AUTO-01**: Add lightweight repository checks for Markdown structure and broken internal links.
- **AUTO-02**: Add a helper that reports study progress without changing it.
- **AUTO-03**: Add templates or scripts for creating new lab/runbook/source-map artifacts.

### Advanced Labs

- **ADV-01**: Add source-driven Go labs for Kubernetes scheduler or kubelet concepts.
- **ADV-02**: Add C/C++ or dynamic-linking labs relevant to HAMi memory isolation.
- **ADV-03**: Add topology-aware scheduling experiments related to Volcano and DRA concepts.

## Out of Scope

Explicitly excluded. Documented to prevent scope creep.

| Feature | Reason |
|---------|--------|
| Replacing the LFX 10-day roadmap | The roadmap is the learning curriculum and already exists in `roadmap/LFX_10_DAY_ROADMAP.md`. |
| Marking Day 1 or any study day complete during GSD initialization | Study completion requires real evidence, teach-back, quiz, and exit criteria. |
| Fabricating experiment output or benchmarks | The repository is an evidence record, not a generated portfolio facade. |
| Building a generic SaaS/product app as v1 | The current objective is the infra study and implementation workspace. |
| Requiring multi-GPU or paid cloud infrastructure for initial labs | Most foundational concepts can be learned locally or through controlled simulation. |

## Traceability

Which phases cover which requirements. Updated during roadmap creation.

| Requirement | Phase | Status |
|-------------|-------|--------|
| GOV-01 | Phase 1 | Pending |
| GOV-02 | Phase 1 | Pending |
| GOV-03 | Phase 1 | Pending |
| GOV-04 | Phase 1 | Pending |
| EVID-01 | Phase 2 | Pending |
| EVID-02 | Phase 2 | Pending |
| EVID-03 | Phase 2 | Pending |
| EVID-04 | Phase 2 | Pending |
| LAB-01 | Phase 3 | Pending |
| LAB-02 | Phase 3 | Pending |
| LAB-03 | Phase 3 | Pending |
| LAB-04 | Phase 3 | Pending |
| SRC-01 | Phase 4 | Pending |
| SRC-02 | Phase 4 | Pending |
| SRC-03 | Phase 4 | Pending |
| VER-01 | Phase 5 | Pending |
| VER-02 | Phase 5 | Pending |
| VER-03 | Phase 5 | Pending |
| VER-04 | Phase 5 | Pending |
| RECALL-01 | Phase 6 | Pending |
| RECALL-02 | Phase 6 | Pending |
| RECALL-03 | Phase 6 | Pending |

**Coverage:**
- v1 requirements: 22 total
- Mapped to phases: 22
- Unmapped: 0

---
*Requirements defined: 2026-08-26*
*Last updated: 2026-08-26 after initial definition*
