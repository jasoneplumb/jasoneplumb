# Jason Plumb

Systems-performance engineer. The projects below demonstrate embedded determinism, autonomous authorization, production web systems, hardware/firmware, and applied ML.

## Projects

**[cue](https://github.com/jasoneplumb/cue)** — Deterministic decision kernel for cycling safety. The same C99 kernel runs live on iPhone, as an MCU actuator, and in offline replay; all three agree bit-for-bit. Field record: 11,300 shadow-compared real-world steps with zero divergences; 23/23 ride traces replay exactly. [Field results](https://github.com/jasoneplumb/cue/blob/mainline/docs/results.md).

**[exe-auth-ctrl-loop](https://github.com/jasoneplumb/exe-auth-ctrl-loop)** — Cross-model execution-authority control loop integrating OpenAI proposals with Claude execution through deterministic, fail-closed authorization. Research prototype with runnable offline examples and explicit production limitations. [Example code](https://github.com/jasoneplumb/exe-auth-ctrl-loop/blob/mainline/examples/example.py).

**[webmap.dev](https://www.webmap.dev)** — Progressive Web App for GPS navigation and offline map exploration. Mobile-first design with turn-by-turn routing, offline tile caching, and background GPS keepalive. Bundle size ≤103 kB gzipped. [Live app](https://www.webmap.dev).

**[infobento.com](https://github.com/jasoneplumb/infobento.com)** — eInk display showing only the data you want — date, weather forecast, air quality — without unlocking your phone. ESP32-C3 firmware plus TypeScript/Node web backend. [Live site](https://www.infobento.com).

**[FIW](https://github.com/jasoneplumb/FIW)** — Kinship verification from facial images using a Siamese CNN with a pretrained FaceNet backbone (Families in the Wild). PyTorch; AUC-ROC 0.674. [Kaggle competition](https://www.kaggle.com/c/recognizing-faces-in-the-wild).
