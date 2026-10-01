# Jason E. Plumb

**Systems Architect · Agentic Engineering · Embedded Firmware · Observability**

I build systems where behavior can be inspected, measured, tested, and replayed.

Across 26 years at Intel, I worked on developer platforms, embedded firmware, spatial computing, computer vision, graphics, performance analysis, and observability. The recurring problem was the same: turn complex system behavior into explicit interfaces and evidence engineers can act on.

My current work applies that discipline to agentic engineering: **probabilistic exploration inside deterministic, evidence-bearing boundaries**. Models can explore and implement; tests, replay, hardware behavior, policy, and human review decide what is accepted.

[Website](https://www.jasoneplumb.com/) · [LinkedIn](https://www.linkedin.com/in/jasoneplumb/) · [Resume](https://www.jasoneplumb.com/resume.pdf)

## Selected work

### [FIW](https://github.com/jasoneplumb/FIW) — measurement-driven machine learning
Kinship verification using frozen face encoders and a lightweight learned head. Measurement changed the architecture: fine-tuning underperformed the simpler frozen-encoder path. Family-disjoint held-out AUC-ROC: **0.784**.

### [webmap.dev](https://github.com/jasoneplumb/webmap.dev) — offline GPS navigation
A production TypeScript PWA for trail navigation and map exploration. Cached maps and live GPS position continue without connectivity; search and route calculation use the network. Designed, built, and operated independently.

### [Execution Authority Control Loop](https://github.com/jasoneplumb/exe-auth-ctrl-loop) — controlled execution for AI agents
A fail-closed research prototype that separates model proposals from authority to create effects. A host-owned deterministic controller applies policy and issues narrowly scoped, single-use capabilities through the only execution gateway. [Paper / DOI](https://doi.org/10.5281/zenodo.21894658).

### [cue](https://github.com/jasoneplumb/cue) — deterministic embedded decision making
One allocation-free C99 decision kernel runs live on a phone, on microcontroller targets, and in offline replay. The current field corpus records **11,300 shadow-compared steps with zero divergences**, with **23/23 traces replaying exactly**. Agreement demonstrates execution consistency, not correctness or safety.

## Additional public engineering artifacts

### [cyclescope](https://github.com/jasoneplumb/cyclescope)
Lightweight C++20 scope/function tracing with per-thread bounded buffers and Perfetto-compatible output. CI includes ThreadSanitizer coverage.

### [taskloom](https://github.com/jasoneplumb/taskloom)
Header-only C++20 concurrency building blocks centered on a Chase-Lev work-stealing deque, with explicit memory-ordering contracts and concurrency testing.

## Earlier systems work

At Intel, I worked across:

- performance analysis and observability, including timeline visualization, tracing, sampling, compiler-assisted instrumentation, ETW, symbolic stacks, DXR, and GPU memory analysis;
- RealSense firmware, SDK/API design, sensor pipelines, IMU capability, and 3D scanning workflows;
- pre-silicon firmware, emulation, SDKs, host/device messaging, lock-free scheduling, and OpenCL simulation for Larrabee;
- early camera-driven spatial-computing architectures, Shockwave 3D, and technology standardized as ECMA-363 Universal 3D.

I hold eight US patents across six inventions, including **Portable Virtual Reality (US 7,113,618)**, **Augmented Reality System (US 7,301,547)**, and **Relational Modeling for Performance Analysis of Multi-Core Processors (US 8,826,234)**.

## How I work

### Intent before implementation

Use structured design conversations to turn an initial idea into explicit requirements and durable design artifacts before implementation begins.

### Artifacts as interfaces

Separate design, implementation, and verification contexts with versioned artifacts rather than depending on conversational memory or implicit model state.

### Probabilistic implementation, deterministic verification

Let AI explore broadly and implement quickly, but establish acceptance independently through tests, simulation, deterministic replay, hardware-in-the-loop validation, CI, and human review.

### Capability without implicit authority

Separate what a model can propose from what it is allowed to execute. Consequential effects cross explicit policy and control boundaries.


Based in Portland, Oregon and Berkeley, California.
