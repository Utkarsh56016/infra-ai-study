# LFX 10-Day Ramp-Up Roadmap

## Day 1 — Kubernetes Mental Model
Pod lifecycle, control plane vs worker, kube-apiserver, scheduler, kubelet, CRI, controller reconciliation.

## Day 2 — Container Runtime Path
OCI, CRI, containerd, runc, kubelet/runtime boundary.

## Day 3 — Linux Process Internals
fork, execve, environment inheritance, PID trees, namespaces, cgroups v2, /proc, dynamic linker.

## Day 4 — NVIDIA GPU Stack
NVIDIA driver, CUDA runtime, NVML, device nodes, nvidia-smi, NVIDIA Container Toolkit.

## Day 5 — Kubernetes GPU Resource Model
Extended resources, Device Plugin API, kubelet device manager, NVIDIA Device Plugin, GPU Operator, scheduling.

## Day 6 — HAMi Observability
Prometheus, labels/cardinality, PromQL, Grafana, allocation vs utilization, GPU memory usage, alerts.

## Day 7 — HAMi Memory Isolation
GPU sharing, child/SSH processes, environment propagation, LD_PRELOAD, CUDA/NVML interception, HAMi-core.

## Day 8 — Volcano Topology-Aware Scheduling
Filter/Score/Reserve/Permit/Bind, topology, NVLink, NVSwitch, NUMA, DRA, ResourceClaim, ResourceSlice.

## Day 9 — Go, C/C++, and Upstream Code
Go foundations, systems C/C++, HAMi/Volcano source navigation, build/test.

## Day 10 — Integration
Trace the complete workload path from Pod to GPU and explain HAMi/Volcano integration points.
