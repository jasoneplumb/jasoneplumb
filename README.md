# Jason E. Plumb

**Embedded Systems & Firmware Architect · Pre-Silicon, Drivers, SDKs · Performance Engineering & Telemetry**

I build embedded systems and the tools that let engineers see what those systems are actually doing. During 26 years at Intel I worked across firmware, device drivers, runtimes, SDKs, and developer tools — production firmware and SDK components for RealSense™ depth cameras, pre-silicon firmware and emulation for Larrabee, and sixteen years of instrumentation and performance analysis. The through-line is turning system behavior into information engineers can act on.

My current projects apply that to behavior you can inspect, test, and replay: a C kernel that must decide identically on a phone, a microcontroller, and in offline replay; deterministic authorization around AI-generated actions; software that keeps working when the network doesn't.

[Résumé and contact](https://www.jasoneplumb.com/) · [LinkedIn](https://www.linkedin.com/in/jasoneplumb/) · [Patents](https://patents.justia.com/inventor/jason-e-plumb)

**Where to start:** embedded and performance → [cue](https://github.com/jasoneplumb/cue), then [InfoBento](https://github.com/jasoneplumb/infobento.com) · AI systems → [exe-auth-ctrl-loop](https://github.com/jasoneplumb/exe-auth-ctrl-loop) · shipped product → [webmap.dev](https://github.com/jasoneplumb/webmap.dev) · machine learning → [FIW](https://github.com/jasoneplumb/FIW). Every repository carries an evidence block stating contribution, status, what was measured, how to reproduce it, and what it does not establish.

## Selected work

### Embedded systems and execution consistency

**[cue](https://github.com/jasoneplumb/cue)** — A deterministic, allocation-free C99 decision kernel compiled into three runtimes: live on iOS, as an MCU actuator, and in offline replay. Over a private 23-trace field corpus the record is 11,301 steps logged, 11,300 compared, zero divergences, and 23/23 traces replaying exactly. That is execution consistency, not correctness or safety — the same record carries the uncompared tail step, the 22 of 49 dispatches with no confirmed delivery, and a policy change that failed. Sole author; AI-assisted under replay and hardware-in-the-loop gates.
[Case study](https://www.jasoneplumb.com/case-studies/cue-equivalence-contract.html) · [Field results](https://github.com/jasoneplumb/cue/blob/mainline/docs/results.md) · [Re-verification](https://github.com/jasoneplumb/cue/blob/mainline/docs/field-reverification.md)

**[infobento.com](https://github.com/jasoneplumb/infobento.com)** — eInk display firmware plus a TypeScript/Node web service. Firmware is bench-verified on a reTerminal E1001 (ESP32-S3): provisioning, conditional refresh, deep sleep, dual-orientation caching, recovery, factory reset. The production ESP32-C3 port and the solar power budget are design targets — deep-sleep current sits below the bench meter's 10 mA resolution and is not yet measured.
[Bench record](https://github.com/jasoneplumb/infobento.com/blob/mainline/firmware/README.md)

### AI systems with explicit execution boundaries

**[exe-auth-ctrl-loop](https://github.com/jasoneplumb/exe-auth-ctrl-loop)** — A research prototype where OpenAI proposes, Claude requests execution, and a host-owned deterministic controller decides: capabilities bound to one proposal digest, one tool, one effect set, one use. `python examples/denials.py` runs offline and shows six requests producing one effect — stale evidence, sparse evidence, an unresolved question, edited arguments, and a replayed capability each refused. Production isolation and durable state are documented as missing.
[Problem, demo, and limits](https://github.com/jasoneplumb/exe-auth-ctrl-loop#in-one-minute) · [Disclosure DOI](https://doi.org/10.5281/zenodo.21894658)

### Product engineering

**[webmap.dev](https://github.com/jasoneplumb/webmap.dev)** — A TypeScript PWA for GPS navigation and offline map exploration, live and in use. Cached maps and position work without connectivity; search and routing need the network. Main JS chunk measures 126.39 kB gzipped at v0.50.0 against a 150 kB CI-enforced budget. Designed, built, and operated solo.
[Live app](https://www.webmap.dev) · [Architecture](https://github.com/jasoneplumb/webmap.dev/blob/mainline/docs/architecture.md)

### Measurement-driven machine learning

**[FIW](https://github.com/jasoneplumb/FIW)** — Kinship verification on Families in the Wild: three frozen face encoders rank-blended by a 6,145-parameter linear head, adopted after measurement showed fine-tuning scored *below* the unmodified encoder zero-shot. Repository reports AUC-ROC 0.784 on a 23,776-pair family-disjoint held-out split — short of its 0.80 target, and published with the protocol caveats that comparison carries.
[Methods and results](https://github.com/jasoneplumb/FIW/blob/mainline/README.md)

### Performance engineering (Intel, not public)

Sixteen years of instrumentation and analysis work — Intel ITT scoped tracing and RAII wrappers, compiler-inserted `_penter`/`_pexit` hooks that reconstruct call graphs without touching user code, ETW kernel-event capture, DXR test harnesses, and steady-state frame partitioning for D3D12/Vulkan captures. The code and measurements are Intel's. [This case study](https://www.jasoneplumb.com/case-studies/compiler-automated-instrumentation.html) explains the approach and is explicit about which parts a reader can verify and which rest on my own account.

---

Based in Portland, Oregon. Open to architecture, embedded systems, firmware, performance engineering, and developer-tool roles — full-time, part-time, or consulting, including remote work nationwide.
