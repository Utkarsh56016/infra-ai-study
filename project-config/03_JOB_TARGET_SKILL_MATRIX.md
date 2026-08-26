# Job Target Skill Matrix

## Target Role 1 — AI / GPU Infrastructure Engineer
Must be strong: Linux, Kubernetes, containers, NVIDIA GPU stack, GPU scheduling, observability, inference deployment, networking, storage, debugging.

High-value depth: Device Plugins, DRA, GPU sharing, MIG, topology, NVLink/NVSwitch, DCGM, Prometheus, vLLM, scheduler internals.

## Target Role 2 — MLOps Engineer
Must be strong: Python, Docker, Kubernetes, CI/CD, MLflow, model serving, observability, deployment validation, cloud fundamentals, model lifecycle.

Interview areas: deployment, rollback, registry, reproducibility, inference scaling, monitoring, GPU vs CPU tradeoffs.

## Target Role 3 — Platform Engineer
Must be strong: Linux, Kubernetes, networking, storage, systemd, containers, monitoring, automation, incident debugging.

High-value depth: control plane, etcd, ingress, DNS, TLS/PKI, CNI, CSI, HA, capacity management.

## Target Role 4 — Kubernetes / Cloud-Native Engineer
Must be strong: API objects, controllers, scheduler, kubelet, CRI, CNI, CSI, Services, Ingress, RBAC, TLS, debugging.

Growth area: Go as a real working language.

## Target Role 5 — Backend AI Engineer
Must be strong: Python, FastAPI, async programming, APIs, LLM serving, RAG, observability, Docker, databases, caching, reliability.

## Shared Foundation
Linux → Containers → Kubernetes → Platform → AI Infrastructure

### Linux
processes, memory, filesystems, networking, systemd

### Containers
OCI, namespaces, cgroups, containerd/runc

### Kubernetes
API, scheduler, kubelet, networking, storage

### Platform
observability, HA, security, automation

### AI Infrastructure
GPU, inference, scheduling, model operations

## Priority Gaps
Tier 1: Go, scheduler internals, Linux process internals, container runtime internals, GPU device/resource model.

Tier 2: cloud networking, controllers/operators, DRA, topology-aware scheduling, advanced PromQL, OpenTelemetry.

Tier 3: deeper C/C++, eBPF fundamentals, service mesh internals, confidential containers, distributed training infrastructure.

## Interview Preparation Mode
Prefer realistic questions based on Utkarsh's actual experience, e.g.:

“A GPU Pod is Pending despite a healthy GPU node. Walk through your debugging.”

Sessions should include:
1. system design
2. debugging
3. fundamentals
4. resume deep dive
5. project defense
6. Linux/Kubernetes commands
7. tradeoff discussion
