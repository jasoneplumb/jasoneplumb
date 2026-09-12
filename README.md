# Jason Plumb

Systems-performance engineer. Three projects demonstrate embedded determinism, autonomous authorization, and production web systems.

## Projects

**[cue](https://github.com/jasoneplumb/cue)** — Deterministic decision kernel for cycling safety. The same C99 kernel runs live on iPhone, as an MCU actuator, and in offline replay; all three agree bit-for-bit. Field record: 11,300 shadow-compared real-world steps with zero divergences; 23/23 ride traces replay exactly. [Field results](https://github.com/jasoneplumb/cue/blob/mainline/docs/results.md).

**[exe-auth-ctrl-loop](https://github.com/jasoneplumb/exe-auth-ctrl-loop)** — Cross-model execution-authority control loop integrating OpenAI proposals with Claude execution through deterministic, fail-closed authorization. Research prototype with runnable offline examples and explicit production limitations. [Example code](https://github.com/jasoneplumb/exe-auth-ctrl-loop/blob/mainline/examples/example.py).

**[webmap.dev](https://www.webmap.dev)** — Progressive Web App for GPS navigation and offline map exploration. Mobile-first design with turn-by-turn routing, offline tile caching, and background GPS keepalive. Bundle size ≤103 kB gzipped. [Live app](https://www.webmap.dev).
