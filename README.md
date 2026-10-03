# Jason E. Plumb

**Systems & Performance Architect · Edge AI · Embedded Systems · Computer Vision**

I work on performance-sensitive systems where the useful question is not just *is it fast?* but *where is the time going, what resource is limiting it, and did the optimization preserve the intended result?*

Across 26 years at Intel, I worked on GPU performance tooling, low-overhead instrumentation, developer platforms, embedded and sensor systems, pre-silicon software, computer vision, and runtime systems. My current work extends that approach into machine-learning evaluation, embedded execution, concurrency, tracing, and AI-assisted engineering.

[Website](https://www.jasoneplumb.com/) · [LinkedIn](https://www.linkedin.com/in/jasoneplumb/) · [Resume](https://www.jasoneplumb.com/resume.pdf)

## Performance and inference-relevant work

### [cyclescope](https://github.com/jasoneplumb/cyclescope) — low-overhead C++ tracing
C++20 scope/function tracing with per-thread bounded buffers, Perfetto-compatible output, ThreadSanitizer coverage, and explicit overhead benchmarks against untraced twins.

### [taskloom](https://github.com/jasoneplumb/taskloom) — concurrency and runtime primitives
Header-only C++20 building blocks centered on a Chase-Lev work-stealing deque, plus dependency events, streaming statistics, false-sharing isolation, and low-level hardware helpers with explicit memory-ordering contracts.

### [FIW](https://github.com/jasoneplumb/FIW) — measurement-driven machine learning
Kinship verification using frozen face encoders and a lightweight learned head. Evaluation changed the architecture: fine-tuning underperformed the simpler frozen-encoder path. Family-disjoint held-out AUC-ROC: **0.784**.

### [cue](https://github.com/jasoneplumb/cue) — deterministic embedded execution
One allocation-free C99 decision kernel runs in a phone shadow path, on microcontroller targets, and in offline replay. Recorded field traces, cross-architecture CI, and hardware-in-the-loop tests verify execution equivalence.

## Other selected work

### [webmap.dev](https://github.com/jasoneplumb/webmap.dev)
Production TypeScript PWA for trail navigation and map exploration, with offline maps and live GPS position.

### [Execution Authority Control Loop](https://github.com/jasoneplumb/exe-auth-ctrl-loop)
Deterministic host-owned control for AI-initiated effects, with policy applied outside the models. [Paper / DOI](https://doi.org/10.5281/zenodo.21894658).

## Earlier systems work

At Intel, I worked across:

- performance analysis and observability: timeline visualization, tracing, sampling, compiler-assisted instrumentation, ETW, symbolic stacks, DXR, and GPU memory analysis;
- RealSense firmware, SDK/API design, sensor pipelines, IMU capability, and 3D scanning workflows;
- pre-silicon firmware, emulation, SDKs, host/device messaging, lock-free scheduling, and OpenCL simulation for Larrabee;
- camera-driven spatial computing, 3D graphics, and technology standardized as ECMA-363 Universal 3D.

I hold eight US patents across six inventions, including **Portable Virtual Reality (US 7,113,618)**, **Augmented Reality System (US 7,301,547)**, and **Relational Modeling for Performance Analysis of Multi-Core Processors (US 8,826,234)**.

## Engineering approach

1. Freeze a representative workload and correctness check.
2. Define the latency or throughput boundary precisely.
3. Instrument enough of the pipeline to explain the baseline.
4. Distinguish compute, memory, synchronization, and data-movement limits.
5. Optimize the measured bottleneck rather than the most interesting code.
6. Rerun the same workload and correctness checks after each material change.
