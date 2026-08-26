# Source Index

Recommended project source files:

1. `00_PROJECT_CONTEXT.md` — background, current LFX applications, internship and project context.
2. `01_STUDY_OPERATING_SYSTEM.md` — how guided study sessions should run.
3. `02_LFX_10_DAY_ROADMAP.md` — immediate LFX ramp-up plan.
4. `03_JOB_TARGET_SKILL_MATRIX.md` — long-term role preparation.
5. `04_PROJECT_CUSTOM_INSTRUCTIONS.md` — canonical ChatGPT project operating instructions.
6. `05_SOURCE_INDEX.md` — source/mirror index.
7. `06_GITHUB_STUDY_WORKFLOW.md` — persistent GitHub evidence and progress workflow.
8. `GSD_README.md` — supplied GSD Core reference used for Codex build workflow.
9. `07_GSD_CODEX_WORKFLOW.md` — project-specific integration of GSD Core with Codex and the study tracker.

For Project Custom Instructions, use `04_PROJECT_CUSTOM_INSTRUCTIONS.md` as the canonical text for the project's instruction field.

## GitHub mappings

| Project source / rule | GitHub path |
|---|---|
| `00_PROJECT_CONTEXT.md` | `project-config/00_PROJECT_CONTEXT.md` |
| `01_STUDY_OPERATING_SYSTEM.md` | `project-config/01_STUDY_OPERATING_SYSTEM.md` |
| `02_LFX_10_DAY_ROADMAP.md` | `roadmap/LFX_10_DAY_ROADMAP.md` |
| `03_JOB_TARGET_SKILL_MATRIX.md` | `project-config/03_JOB_TARGET_SKILL_MATRIX.md` |
| `04_PROJECT_CUSTOM_INSTRUCTIONS.md` | `project-config/04_PROJECT_CUSTOM_INSTRUCTIONS.md` |
| `05_SOURCE_INDEX.md` | `project-config/05_SOURCE_INDEX.md` |
| `06_GITHUB_STUDY_WORKFLOW.md` | `project-config/06_GITHUB_STUDY_WORKFLOW.md` |
| `GSD_README.md` | `project-config/GSD_README.md` |
| project-specific GSD/Codex rule | `project-config/07_GSD_CODEX_WORKFLOW.md` |

Root `AGENTS.md` is the repository-local entrypoint for Codex. It points Codex to the current tracker, project context, and GSD workflow without duplicating dynamic progress state.

Keep the interactive HTML roadmap on GitHub Pages as the visual tracker when used. The Markdown roadmap is the semantic roadmap used while teaching.
