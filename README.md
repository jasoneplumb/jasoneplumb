# Jason E. Plumb

I work on performance-sensitive systems where the useful question is not just *is it fast?* but *where is the time going, what resource is limiting it, and did the optimization preserve the intended result?*

Across 26 years at Intel, I worked on GPU performance tooling, low-overhead instrumentation, developer platforms, embedded and sensor systems, pre-silicon software, computer vision, and runtime systems. My current work extends that approach into machine-learning evaluation, embedded execution, concurrency, tracing, and AI-assisted engineering.

[Website](https://www.jasoneplumb.com/) · [LinkedIn](https://www.linkedin.com/in/jasoneplumb/)

## Performance and inference-relevant work

### [cyclescope](https://github.com/jasoneplumb/cyclescope) — low-overhead C++ tracing
C++20 scope/function tracing with per-thread bounded buffers, Perfetto-compatible output, ThreadSanitizer coverage, and explicit overhead benchmarks against an untraced twin.

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

## Engineering approach

1. Freeze a representative workload and correctness check.
2. Define the latency or throughput boundary precisely.
3. Instrument enough of the pipeline to explain the baseline.
4. Distinguish compute, memory, synchronization, and data-movement limits.
5. Optimize the measured bottleneck rather than the most interesting code.
6. Rerun the same workload and correctness checks after each material change.
   
## Earlier systems work

At Intel, I worked across:

- Performance analysis and observability: timeline visualization, tracing, sampling, compiler-assisted instrumentation, ETW, symbolic stacks, DXR, and GPU memory analysis
- Intel(R) RealSense(TM) firmware, SDK/API design, sensor pipelines, IMU capability, and 3D scanning workflows
- Pre-silicon firmware, emulation, SDKs, host/device messaging, lock-free scheduling, and OpenCL simulation for Larrabee
- Camera-driven spatial computing, 3D graphics, and technology standardized as ECMA-363 Universal 3D

Patents:

- **US 6771841: Determining a bounding shape for a collection of points**
- **US 6927757: Camera driven virtual workspace management**
- **US 6975328, 7098925, 7245305: Shading of images using texture**
- **US 7113618: Portable Virtual Reality**
- **US 7301547: Augmented Reality System**
- **US 8826234: Relational Modeling for Performance Analysis of Multi-Core Processors**
