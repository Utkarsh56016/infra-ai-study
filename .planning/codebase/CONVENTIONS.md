---
last_mapped_commit: 798de18a326e179f27a289fe0f1c786a04380007
---

# Conventions

**Analysis Date:** 2026-08-26

## Summary

The repository conventions are documentation and evidence conventions rather than programming conventions. The strongest patterns are structured Markdown, explicit progress gates, source-of-truth rules, and separation between study completion and implementation verification.

## Markdown Style

- Files use ATX headings with `#`, `##`, and `###`.
- Root documents start with direct descriptive titles, such as `# Infra & AI Study` and `# Study Progress`.
- Tables are used for progress and source mappings in `README.md`, `PROGRESS.md`, and `project-config/05_SOURCE_INDEX.md`.
- Code blocks are used for system flows, commands, and repository layout.
- Day READMEs use repeated structured sections to keep evidence comparable across days.

## Evidence Labels

`AGENTS.md`, `README.md`, `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md`, `project-config/06_GITHUB_STUDY_WORKFLOW.md`, and `project-config/07_GSD_CODEX_WORKFLOW.md` all reinforce the same evidence boundary:

- **Observed** means supplied by a real command, test, experiment, or inspected source.
- **Expected** means healthy/reference behavior.
- **Inference** means a conclusion supported by observations.
- **Hypothesis** means plausible but unverified.
- **Unknown** means unresolved.

This convention is central to future labs and debugging notes.

## Study Session Pattern

The default study flow appears in `project-config/01_STUDY_OPERATING_SYSTEM.md` and `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md`:

```text
Orientation -> First-Principles Explanation -> Mental Model -> Hands-On Lab
-> Break It -> Debugging Method -> Teach-Back -> Mini Quiz -> Exit Criteria
```

The compact loop is:

```text
Understand -> Visualize -> Build -> Break -> Debug -> Explain -> Recall
```

## GSD Build Pattern

For non-trivial Codex implementation tasks, `AGENTS.md` and `project-config/07_GSD_CODEX_WORKFLOW.md` require:

```text
Discuss -> Plan -> Execute -> Verify -> Ship
```

Read-only investigation, explanations, quizzes, tiny one-file examples, and trivial documentation corrections do not require a GSD phase unless requested.

## Progress Update Convention

- Read `PROGRESS.md` before deciding current progress.
- Read the active day README before updating day state.
- Do not mark a day complete until exit criteria are actually satisfied.
- Keep `PROGRESS.md` tied to validated study milestones.
- Keep GSD implementation artifacts separate from study completion state.

## Commit Convention

`CONTRIBUTING.md` recommends focused, evidence-linked commit messages such as:

- `day01: add Kubernetes pod scheduling flow`
- `day02: trace kubelet to containerd runtime path`
- `day03: add fork-exec environment inheritance lab`

The convention avoids vague commit messages and ties repository history to learning artifacts.

## File Organization Convention

- Day notes stay in `days/day-XX-*/README.md`.
- Substantial labs go under `labs/`.
- Diagrams go under `diagrams/`.
- Debugging procedures go under `runbooks/`.
- Compact references go under `cheatsheets/`.
- Source-code readings go under `source-maps/`.
- Interview preparation goes under `interview-notes/`.

## Safety Convention

- Preserve existing content and directory structure unless restructuring is intentional.
- Read a tracked file before replacing it.
- Do not fabricate terminal output, tests, metrics, quiz results, confidence, or completion.
- Distinguish expected examples from observed outputs.
- Do not overwrite local/uncommitted work blindly.

*Codebase conventions analysis: 2026-08-26*
<!-- refreshed: 2026-08-26 -->
