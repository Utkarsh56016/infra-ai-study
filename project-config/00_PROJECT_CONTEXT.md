# Study: Infra & AI — Project Context

## Purpose
This project is Utkarsh Mishra's long-term guided study workspace for:

1. LFX/CNCF mentorship preparation.
2. GPU / AI infrastructure engineering.
3. Kubernetes and cloud-native systems.
4. Linux and container runtime internals.
5. MLOps / platform engineering interview preparation.
6. Targeted job preparation for MLOps, AI Infrastructure, Platform, Kubernetes/Cloud-Native, Backend AI, and related roles.

The project should optimize for practical competence, not memorization.

## Current LFX Context
Utkarsh has applied to three CNCF/LFX 2026 Term 3 projects:

1. HAMi — GPU Observability: Metrics and Dashboards
2. HAMi — Fix GPU Memory Isolation for Child and SSH Processes
3. Volcano — Generic xPU Topology-Aware Scheduling

The immediate goal is to use the period before the selection window to build a strong systems foundation that remains useful even if no mentorship is awarded.

Shared technical path:

Kubernetes → scheduler / kubelet / CRI → containerd / runc / OCI → Linux processes / namespaces / cgroups → NVIDIA container runtime → CUDA / NVML / GPU → HAMi → Volcano

## Existing Technical Background

### Education
- Final-year Electronics and Communication Engineering student.
- Thapar Institute of Engineering & Technology.
- Expected graduation: 2027.

### Main Career Direction
- MLOps Engineer
- AI Infrastructure Engineer
- GPU Infrastructure Engineer
- Platform Engineer
- Kubernetes / Cloud-Native Engineer
- Backend AI Engineer

### Internship Experience
Completed an MLOps engineering internship at Piramal Finance.

Hands-on exposure included:
- Kubernetes, Kubespray
- NVIDIA H100 NVL
- NVIDIA GPU Operator, KAI Scheduler
- DCGM, Prometheus, Grafana
- containerd, runc, Linux
- Calico VXLAN, kube-proxy IPVS
- NFS CSI, Traefik, JupyterHub
- AWS EC2
- GPU inference workloads
- Kubernetes high availability
- troubleshooting across runtime, networking, storage, TLS, and GPU layers

Important experience:
- Control plane expansion from 1 to 3 nodes.
- etcd expansion and validation.
- Remote H100 worker integration.
- GPU inference validation.
- Runtime/network/storage debugging.
- GPU monitoring and observability.
- vLLM-based inference validation.

### Programming
Strongest:
- Python
- Bash

Working familiarity:
- C

Current growth areas:
- Go
- deeper systems C/C++
- Kubernetes scheduler internals
- GPU runtime internals

## Relevant Portfolio Projects

### GPU Platform Intelligence Agent
Read-only AI infrastructure operations assistant using FastAPI, PostgreSQL, Kubernetes APIs, Prometheus, GPU telemetry, BM25 retrieval, and structured evidence.

Reasoning boundaries:
- Observation
- Inference
- Hypothesis
- Unknown

### Kira
Local-first Linux AI assistant using Python asyncio, Unix socket IPC, deterministic intent routing, ChromaDB, NetworkX, local LLM inference, voice pipeline, and Linux system integrations.

### GPU Accelerated Inference API
PyTorch, FastAPI, Docker, Prometheus, Grafana, Locust, FP16 / GPU performance validation.

### ML Training and Deployment Workflow
PyTorch, MLflow, Docker, Kubernetes/kind, GitHub Actions, deployment validation gates.

## Learning Philosophy
Prefer:
- first principles
- system diagrams
- packet/process/control-flow tracing
- source-code reading
- small reproducible labs
- debugging exercises
- interview-style explanation
- teach-back
- command-line verification

Avoid:
- shallow keyword memorization
- huge passive reading lists
- overloading a day with unrelated topics
- pretending proficiency that has not been demonstrated
