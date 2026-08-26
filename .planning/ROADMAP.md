# Roadmap: Infra AI Study Workspace

## Overview

This roadmap initializes the GSD implementation layer for the AI/GPU infrastructure study repository. It does not replace the LFX learning curriculum in `roadmap/LFX_10_DAY_ROADMAP.md`; instead, it organizes reusable build work that helps the repository accumulate real labs, debugging artifacts, source maps, verification practices, and recall/interview material.

## Phases

**Phase Numbering:**
- Integer phases (1, 2, 3): Planned milestone work
- Decimal phases (2.1, 2.2): Urgent insertions (marked with INSERTED)

- [ ] **Phase 1: Governance Boundary** - Protect the separation between study progress and GSD implementation state.
- [ ] **Phase 2: Evidence Artifact System** - Create reusable evidence patterns for labs, debugging, and study records.
- [ ] **Phase 3: Local Lab Infrastructure** - Build local-first lab scaffolds for Kubernetes, runtime, Linux, GPU, HAMi, and Volcano topics.
- [ ] **Phase 4: Source Mapping Workflow** - Create source-code reading structures for upstream infrastructure projects.
- [ ] **Phase 5: Verification And Progress Guardrails** - Add checks and practices that keep implementation verification separate from study completion.
- [ ] **Phase 6: Recall And Interview Layer** - Add teach-back, quiz, cheat-sheet, and interview artifacts grounded in repository evidence.

## Phase Details

### Phase 1: Governance Boundary
**Goal**: Make the study/GSD boundary explicit in maintained repository artifacts and future workflow entrypoints.
**Depends on**: Nothing (first phase)
**Requirements**: [GOV-01, GOV-02, GOV-03, GOV-04]
**Success Criteria** (what must be TRUE):
  1. The repository documents that `roadmap/LFX_10_DAY_ROADMAP.md` remains the learning curriculum.
  2. The repository documents that `.planning/*` is implementation/build state, not study completion evidence.
  3. Future non-trivial implementation requests have a clear GSD route.
  4. Progress update rules remain tied to validated study evidence.
**Plans**: TBD

Plans:
- [ ] 01-01: Review and strengthen repository workflow boundaries.
- [ ] 01-02: Add or refine references that route future build work through GSD without changing study progress.

### Phase 2: Evidence Artifact System
**Goal**: Establish reusable artifact formats for evidence-backed labs, debugging exercises, and day records.
**Depends on**: Phase 1
**Requirements**: [EVID-01, EVID-02, EVID-03, EVID-04]
**Success Criteria** (what must be TRUE):
  1. Lab and debugging artifacts have a repeatable evidence structure.
  2. Observed, Expected, Inference, Hypothesis, and Unknown are represented clearly.
  3. The Understand -> Visualize -> Build -> Break -> Debug -> Explain -> Recall loop is preserved in artifacts.
  4. Substantial content has clear placement outside overloaded day READMEs.
**Plans**: TBD

Plans:
- [ ] 02-01: Define evidence-first artifact templates.
- [ ] 02-02: Wire template placement into the repository layout.

### Phase 3: Local Lab Infrastructure
**Goal**: Build local-first lab scaffolds that can support hands-on systems learning without expensive infrastructure.
**Depends on**: Phase 2
**Requirements**: [LAB-01, LAB-02, LAB-03, LAB-04]
**Success Criteria** (what must be TRUE):
  1. Lab scaffolds can represent Kubernetes, container runtime, Linux process, GPU, HAMi, and Volcano topics.
  2. Maintained labs include verification commands or manual validation steps.
  3. Labs favor the documented Arch Linux / RTX 3050 target environment where feasible.
  4. Failure/debugging scenarios are captured alongside healthy-path behavior.
**Plans**: TBD

Plans:
- [ ] 03-01: Create the first reusable lab scaffold.
- [ ] 03-02: Add validation and debugging sections to lab artifacts.
- [ ] 03-03: Connect labs to day-level records without marking study completion automatically.

### Phase 4: Source Mapping Workflow
**Goal**: Create source-code reading artifacts for Kubernetes, container runtimes, NVIDIA tooling, HAMi, and Volcano.
**Depends on**: Phase 3
**Requirements**: [SRC-01, SRC-02, SRC-03]
**Success Criteria** (what must be TRUE):
  1. Source maps can record entrypoints, ownership boundaries, test locations, and upstream commands.
  2. Source conclusions distinguish observed inspected source from inference.
  3. The workflow supports future HAMi, Volcano, Kubernetes, containerd, and runc source maps.
**Plans**: TBD

Plans:
- [ ] 04-01: Define source-map artifact structure.
- [ ] 04-02: Add initial upstream source-map placeholders or templates.

### Phase 5: Verification And Progress Guardrails
**Goal**: Add implementation verification and progress guardrails that prevent accidental or fabricated completion.
**Depends on**: Phase 4
**Requirements**: [VER-01, VER-02, VER-03, VER-04]
**Success Criteria** (what must be TRUE):
  1. Implementation phases define verification criteria before completion.
  2. GSD verification does not automatically mark study-day exit criteria complete.
  3. Progress/status files remain conservative when evidence is missing.
  4. Generated docs are checked for obvious secret-shaped content before commit.
**Plans**: TBD

Plans:
- [ ] 05-01: Add verification guidance for maintained implementation artifacts.
- [ ] 05-02: Add conservative progress-update guardrails.
- [ ] 05-03: Add lightweight safety checks for generated documentation.

### Phase 6: Recall And Interview Layer
**Goal**: Build recall and interview-preparation artifacts grounded in real repository evidence.
**Depends on**: Phase 5
**Requirements**: [RECALL-01, RECALL-02, RECALL-03]
**Success Criteria** (what must be TRUE):
  1. Teach-back, quiz, cheat-sheet, and interview-note artifacts have clear homes.
  2. Interview-prep claims trace to real experience or repository evidence.
  3. Final summaries can cite labs, diagrams, runbooks, or source maps.
**Plans**: TBD

Plans:
- [ ] 06-01: Define recall and interview artifact structure.
- [ ] 06-02: Add traceability from summaries back to evidence artifacts.

## Progress

**Execution Order:**
Phases execute in numeric order: 1 -> 2 -> 3 -> 4 -> 5 -> 6

| Phase | Plans Complete | Status | Completed |
|-------|----------------|--------|-----------|
| 1. Governance Boundary | 0/2 | Not started | - |
| 2. Evidence Artifact System | 0/2 | Not started | - |
| 3. Local Lab Infrastructure | 0/3 | Not started | - |
| 4. Source Mapping Workflow | 0/2 | Not started | - |
| 5. Verification And Progress Guardrails | 0/3 | Not started | - |
| 6. Recall And Interview Layer | 0/2 | Not started | - |
