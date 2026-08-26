# GSD Core + Codex Workflow — Study: Infra & AI

## Purpose

This document defines how Codex implementation work is performed inside `Utkarsh56016/infra-ai-study`.

The study system and the coding system are related but not identical:

```text
Study / learning:
Understand → Visualize → Build → Break → Debug → Explain → Recall

Codex implementation:
Discuss → Plan → Execute → Verify → Ship
```

The first loop proves understanding. The second loop controls software-building work.

## GSD is mandatory for Codex building tasks

Use GSD Core for non-trivial Codex implementation work, including:

- multi-file labs
- Python/Go/C/C++ implementations
- Kubernetes tooling
- scheduler/runtime experiments that produce reusable code
- automation/scripts that become maintained project artifacts
- controllers/operators/plugins
- substantial refactors
- production-style portfolio implementations
- changes where architecture, dependencies, testing, or rollback need explicit planning

Do not jump directly from a broad request to unrestricted coding.

Read-only source inspection, conceptual explanations, quizzes, teach-backs, tiny one-file examples, and trivial documentation corrections do not require a GSD phase unless explicitly requested.

## GSD phase loop

GSD Core defines five stages:

1. **Discuss** — capture implementation decisions before planning.
2. **Plan** — research and decompose the phase into executable work.
3. **Execute** — implement the approved plans in controlled waves.
4. **Verify** — test and walk through what was built; diagnose gaps before declaring success.
5. **Ship** — create the delivery/PR, archive the phase, and move forward.

Do not skip Verify merely because code compiles or a happy-path test passes.

## Existing-repository onboarding

This is an existing repository. GSD Core should be installed with the official installer for the Codex runtime rather than by copying framework files manually.

Installer command from the supplied GSD README:

```bash
npx @opengsd/gsd-core@latest
```

Choose:

- runtime: **Codex**
- installation scope: **local/project** for this repository

Then onboard the existing repository:

```text
/gsd-onboard
```

The GSD-generated `.planning/` tree becomes the persistent state for implementation phases.

## Planning-state boundary

GSD planning state is implementation state, not evidence that a study topic is complete.

Examples:

```text
.planning/PROJECT.md      → project/build understanding
.planning/ROADMAP.md      → implementation milestone/phase plan
.planning/STATE.md        → current GSD execution state
.planning/phases/...      → phase context, research, plans, summaries
```

These artifacts must be generated/maintained through the GSD workflow. Do not fabricate their contents merely to make the repository appear initialized.

## Relationship to the study tracker

A build can support a study exit criterion, but the two gates remain separate.

Example:

```text
Day 3 study goal
   ↓
Design fork/exec experiment
   ↓
If implementation is substantial → GSD phase
   ↓
Execute + verify code through GSD
   ↓
Utkarsh runs/inspects real experiment evidence
   ↓
Teach-back + quiz + roadmap exit criteria
   ↓
Only then update Day 3 completion state
```

GSD `Verify` answers: **Did we build the implementation correctly?**

Study exit criteria answer: **Does Utkarsh understand, debug, and explain the system?**

Passing one does not automatically pass the other.

## Codex startup sequence

When Codex opens this repository:

1. Read root `AGENTS.md`.
2. Read `README.md` and `PROGRESS.md`.
3. Read the current day README and `roadmap/LFX_10_DAY_ROADMAP.md`.
4. Read relevant `project-config/` documents.
5. For implementation work, inspect `.planning/` if it exists.
6. If GSD is not initialized and a build task is requested, onboard through GSD before broad implementation.
7. Inspect existing architecture before proposing changes.
8. Prefer small, verifiable changes.

## Evidence and verification rules

Never record as fact:

- tests that were not run
- command output that was not observed
- benchmarks that were not measured
- successful builds that were not verified
- root causes without evidence
- study completion inferred only from generated code

Use:

- **Observed**
- **Expected**
- **Inference**
- **Hypothesis**
- **Unknown**

## Git and repository rules

- Read existing files before replacing them.
- Preserve user changes.
- Keep commits focused.
- Do not mix unrelated roadmap progress with implementation commits.
- Keep reusable build artifacts in their appropriate directories.
- Update `PROGRESS.md` only after real study progress has been validated.
- Treat GitHub as the persistent engineering source of truth.

## Source

This integration is based on the project-provided `GSD_README.md`, which describes GSD Core as a context-engineering/spec-driven framework compatible with Codex and defines the Discuss → Plan → Execute → Verify → Ship phase loop.
