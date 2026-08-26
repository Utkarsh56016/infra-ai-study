# LFX 10-Day Ramp-Up Roadmap

## Goal
Become fluent enough in the shared HAMi / Volcano / GPU infrastructure foundations to:
- ramp quickly if selected
- hold a technical discussion with a mentor
- read upstream code without fear
- retain the knowledge as durable career capital if not selected

## Day 1 — Kubernetes Mental Model
Topics: Pod lifecycle, control plane vs worker, kube-apiserver, scheduler, kubelet, CRI, controller reconciliation, workload control flow.

Output: draw `kubectl → API Server → Scheduler → Node → Kubelet → CRI → Runtime` from memory.

Exit test: explain how a newly created Pod reaches a worker node.

## Day 2 — Container Runtime Path
Topics: OCI image/runtime concepts, CRI, containerd, runc, kubelet/runtime responsibility boundary.

Output: trace `PodSpec → kubelet → CRI request → containerd → OCI bundle → runc → Linux process`.

Lab: inspect containers, processes, namespaces, and runtime metadata locally.

## Day 3 — Linux Process Internals
Topics: fork, execve, environment inheritance, PID tree, namespaces, cgroups v2, /proc, dynamic linker basics.

Output: small parent→child environment inheritance experiment.

Exit test: explain what changes and survives across fork + exec.

## Day 4 — NVIDIA GPU Stack
Topics: NVIDIA driver, CUDA runtime, NVML, device nodes, nvidia-smi, NVIDIA Container Toolkit, GPU visibility inside containers.

Exit test: explain why CUDA, the driver, NVML, and nvidia-smi are different things.

## Day 5 — Kubernetes GPU Resource Model
Topics: extended resources, Device Plugin API, kubelet device manager, NVIDIA Device Plugin, GPU Operator, GPU Pod scheduling, scalar-resource limitation, KAI Scheduler concept.

Exit test: explain how `nvidia.com/gpu: 1` becomes a concrete device inside a container.

## Day 6 — HAMi Observability
Topics: Prometheus metric types, labels/cardinality, PromQL, Grafana dashboards, allocation vs utilization, memory requested vs used, alerts, SLO thinking, OpenTelemetry concepts.

Output: at least five PromQL queries or pseudo-queries for GPU platform health.

## Day 7 — HAMi Memory Isolation
Topics: HAMi GPU sharing, process-level enforcement, child process behavior, SSH-created processes, environment propagation, dynamic linking / LD_PRELOAD concept, CUDA/NVML interception concepts, HAMi-core, reproduction methodology.

Core path: `Kubernetes → containerd/runc → container → process environment → HAMi-core → CUDA/NVML → GPU`.

Output: debugging checklist for “original process respects GPU memory limit, later process does not.”

## Day 8 — Volcano Topology-Aware Scheduling
Topics: scheduling cycle, Filter, Score, Reserve, Permit, Bind, scheduler cache, gang scheduling, topology-aware placement, concrete device selection, NVLink, NVSwitch, NUMA basics, Kubernetes DRA, ResourceClaim, ResourceSlice, Device Plugin vs DRA.

Exit test: explain the difference between “Node has 8 GPUs” and “only these 4 satisfy topology requirements.”

## Day 9 — Go, C/C++, and Upstream Code
Go target: packages, structs, interfaces, receivers, pointers, slices, maps, errors, context, defer, goroutines, channels, tests.

C/C++ refresh: pointers, memory, structs, function pointers, shared libraries, threads, mutexes, dynamic linking, process APIs.

Upstream work: clone HAMi and Volcano; find entrypoints, plugin registration, metrics, tests, core structures, build instructions; run at least one build or test.

## Day 10 — Integration
From memory draw:
`Pod/workload → scheduler → GPU policy → kubelet/Device Plugin → CRI → containerd → runc → Linux process → NVIDIA runtime/driver/NVML → GPU`.

Then explain:
- where HAMi observability lives
- where HAMi memory isolation can break
- where Volcano placement and topology logic lives

Final outputs:
- one-page GPU infrastructure cheat sheet
- HAMi code map
- Volcano code map
- mentor questions
- 10 interview questions with answers
- remaining gaps
