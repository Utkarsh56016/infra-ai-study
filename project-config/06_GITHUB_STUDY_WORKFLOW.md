# GitHub Study Workflow — Study: Infra & AI

## Purpose

This document defines how ChatGPT and Utkarsh use the GitHub repository:

`Utkarsh56016/infra-ai-study`

The repository is the persistent engineering notebook and progress tracker for the Study: Infra & AI project.

It is not meant to be a dump of copied notes. It should contain evidence of understanding, experiments, debugging, and implementation.

---

## 1. Repository Role

GitHub is the durable source of truth for:

- current study progress
- completed roadmap days
- unfinished concepts
- labs
- experiment results
- diagrams
- debugging investigations
- runbooks
- PromQL
- Kubernetes manifests
- source-code maps
- interview notes
- teach-back summaries
- quizzes
- final cheat sheets

ChatGPT conversations are the interactive teaching environment.

GitHub is the persistent record.

---

## 2. Core Workflow

```text
Concept
   ↓
First-principles explanation
   ↓
Mental model / diagram
   ↓
Local experiment or lab
   ↓
Real evidence from terminal / VS Code
   ↓
Break or failure scenario
   ↓
Debugging
   ↓
Teach-back
   ↓
Quiz
   ↓
Exit criteria
   ↓
GitHub artifact + progress update
```

A topic is not complete merely because it was discussed.

---

## 3. Source-of-Truth Rule

When resuming work, ChatGPT should inspect the relevant GitHub files before relying on memory.

Primary files:

```text
README.md
PROGRESS.md
roadmap/LFX_10_DAY_ROADMAP.md
days/day-XX-*/README.md
```

If GitHub and conversational memory disagree, prefer the latest verified repository state.

---

## 4. What ChatGPT May Do in the Repository

For `Utkarsh56016/infra-ai-study`, ChatGPT may:

- read tracked files
- inspect progress
- create new text/Markdown artifacts
- update existing text/Markdown files
- update day notes
- update `PROGRESS.md`
- add labs and runbooks
- add source-code maps
- add interview notes
- add manifests/code snippets where supported
- inspect pull requests/issues if used later

Before replacing an existing file, ChatGPT should read the latest version first.

Prefer small targeted commits and changes.

---

## 5. What ChatGPT Must Never Fake

Do not record:

- commands as executed when they were only suggested
- output that Utkarsh did not actually obtain
- benchmarks that were not measured
- passing tests that were not run
- completed exit criteria that were not demonstrated
- root causes without supporting evidence
- proficiency that has not been shown

Use explicit labels when necessary:

- **Observed:** supplied directly by the experiment
- **Expected:** what healthy behavior should look like
- **Inference:** conclusion supported by observations
- **Hypothesis:** plausible but unverified explanation
- **Unknown:** unresolved information

---

## 6. Local Lab Workflow

Most experiments run on Utkarsh's local machine:

- Arch Linux
- HP Victus 15
- Ryzen 5 5600H
- RTX 3050 4 GB
- 16 GB RAM

Normal workflow:

```text
ChatGPT designs experiment
        ↓
Utkarsh creates/runs code in VS Code or terminal
        ↓
Utkarsh shares command/output/error
        ↓
ChatGPT analyzes evidence
        ↓
Experiment is refined if needed
        ↓
Result becomes a repo artifact
        ↓
ChatGPT updates GitHub
```

Do not push a "successful" lab before the actual experiment has been validated.

---

## 7. Recommended Artifact Placement

```text
days/
  day-XX-topic/
    README.md

labs/
  <topic-name>/
    README.md
    code...

diagrams/
  <topic>.md

runbooks/
  <problem>.md

cheatsheets/
  <topic>.md

interview-notes/
  <topic>.md

source-maps/
  hami/
  volcano/
  kubernetes/
```

Use a new artifact when content is substantial enough to stand on its own.

Avoid turning a single README into an unstructured knowledge dump.

---

## 8. Day Completion Protocol

Before a roadmap day is marked complete, verify:

- [ ] mental model can be explained from memory
- [ ] relevant system/control/process flow can be drawn or traced
- [ ] at least one hands-on lab was completed where feasible
- [ ] at least one failure/debugging scenario was handled
- [ ] teach-back was completed
- [ ] quiz was completed
- [ ] exit criteria from the roadmap were satisfied
- [ ] at least one concrete artifact exists
- [ ] day README reflects actual learning
- [ ] `PROGRESS.md` reflects the validated state

Only then change the day status to complete.

---

## 9. Commit Style

Prefer focused commit messages:

```text
day01: add Kubernetes pod scheduling flow
day02: trace kubelet to containerd runtime path
day03: add fork-exec environment inheritance lab
day04: document NVIDIA device visibility path
day05: map device plugin allocation lifecycle
day06: add GPU observability PromQL queries
day07: document child-process isolation reproduction
day08: map Volcano topology scheduling flow
day09: add HAMi source map
day10: complete end-to-end GPU workload trace
```

Avoid vague commits such as:

```text
update notes
changes
stuff
final
```

---

## 10. Resume / Interview Evidence

The repository can become proof-of-work, but only validated work should be used externally.

Useful evidence includes:

- reproducible labs
- architecture diagrams
- source-code maps
- debugging writeups
- benchmark methodology
- PromQL sets
- Kubernetes manifests
- Go/C experiments
- scheduler/runtime traces

Do not convert study exercises into inflated resume claims.

---

## 11. Commands Utkarsh Can Use in Chat

Examples:

```text
start Day 1
continue
check my GitHub progress
read the Day 3 tracker
update today's progress
save this experiment to the repo
create a runbook from this debugging session
add this lab to GitHub
mark Day 4 complete if I passed the exit criteria
quiz me from everything recorded so far
review my HAMi notes from the repo
show me what's still unfinished
```

ChatGPT should resolve these requests using the current repository state.

---

## 12. Safety Rule for Repository Writes

For existing files:

```text
read current version
        ↓
understand existing structure
        ↓
make smallest necessary change
        ↓
write/update
        ↓
report exactly what changed
```

Do not blindly overwrite repository state.

---

## 13. Final Principle

ChatGPT teaches and coordinates.

Utkarsh runs real experiments and develops the understanding.

GitHub records the evidence.

The objective is a repository that demonstrates increasing ability to:

**operate → debug → implement → design**
