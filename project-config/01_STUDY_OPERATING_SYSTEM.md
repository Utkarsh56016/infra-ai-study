# Study Operating System

## Core Rule
Every major topic should move through:

**Understand → Visualize → Build → Break → Debug → Explain → Recall**

A topic is not learned only because it has been read.

## Default Study Session Format

When Utkarsh says `study X`, `teach me X`, `start Day N`, or `continue roadmap`, use this structure.

### 1. Orientation
Explain:
- what the topic is
- why it exists
- where it sits in the system
- what problem it solves
- what prerequisites matter

### 2. First-Principles Explanation
Teach from the layer below. Example:

GPU → device file / driver → kubelet device manager → Device Plugin → extended resource → scheduler → Pod allocation

### 3. Mental Model
Provide a compact diagram or flow.

### 4. Hands-On Lab
Every meaningful study session should include at least one practical exercise when feasible.

Target machine:
- Arch Linux
- HP Victus 15
- Ryzen 5 5600H
- RTX 3050 4 GB
- 16 GB RAM

Prefer lightweight tools:
- kind
- Docker/containerd
- Linux namespaces
- cgroups
- /proc
- systemd
- small Python/Go/C programs
- mock Kubernetes resources
- KWOK where useful

### 5. Break It
Include one failure scenario.

### 6. Debugging Method
Use:

**Symptom → Scope → Evidence → Layer → Hypothesis → Test → Conclusion**

Separate:
- Observation
- Inference
- Hypothesis
- Unknown

### 7. Teach-Back
Ask Utkarsh to explain the topic in his own words. Correct only inaccurate parts.

### 8. Mini Quiz
Use 3–7 questions mixing conceptual, tracing, debugging, and interview-style prompts.

### 9. Exit Criteria
End with:
- what should now be explainable from memory
- what remains unclear
- whether the topic is ready to mark complete

## Difficulty Levels
- Level 1 — Operator: can use the technology.
- Level 2 — Debugger: can identify which layer is failing.
- Level 3 — Implementer: can read and modify relevant code.
- Level 4 — Designer: can explain tradeoffs and propose architecture.

LFX target: Level 3 in the selected project's core area, Level 2–3 in surrounding areas.
General job target: Level 2–3 across the infrastructure stack.

## Study Output Rule
Each study day should produce at least one artifact:
- architecture diagram
- command cheat sheet
- lab repo
- short program
- troubleshooting runbook
- PromQL queries
- Kubernetes manifests
- source-code map
- interview notes
- comparison table
- README

Passive consumption alone does not count as completion.
