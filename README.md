## Juhyeok Park · 박주혁

**Electronic Engineering, Chungbuk National University · B.S. Feb 2027 · applying for Spring 2027 graduate programs in Physical AI**

> LLMs can *talk about* the world but have never *touched* it.
> I tried three ways to make language models act in the physical world, hit the same wall each time,
> and now want to close that gap with signals that language does not carry.

🌐 **[Portfolio — numbers, demos, papers →](https://nonojamjam.github.io/)** · 📄 **[CV (PDF)](https://nonojamjam.github.io/assets/cv/CV_JuhyeokPark_2026-09.pdf)** · ✉️ 2021076023@chungbuk.ac.kr

---

### Three experiments, one wall

| | What I measured | What it showed |
|---|---|---|
| **01 · Noise-robust satellite detection** (capstone, sole ML/code) | Noisy mAP50 **+0.163** (σ=0.3, seed-stable); clean **−0.053** | 97% of the gain is *training on the corrupted signal*; distillation adds +0.005 |
| **02 · An LLM that writes and reads its own wiki** (KAERI · IAA 2026, first author) | **94%** blind agreement between two cross-family graders | Even with the correct node injected, hallucination remained — knowledge access is not the bottleneck |
| **03 · VLM robot commands gated by forward kinematics** (KAERI · KSIIS 2026, first author) | Position error **165.7 → 276.9 mm** when the VLM was *given* joint angles | Language does not carry the physical quantities the task needs; the check has to sit outside the model |

Details, limitations and the interactive pieces are on the [portfolio](https://nonojamjam.github.io/#capstone).

---

### Try it

[![Same noisy satellite tile: baseline finds nothing, the noise-trained model keeps the lock](https://nonojamjam.github.io/assets/profile/noise_slider.gif)](https://nonojamjam.github.io/noise-robust-detection-rkd/)

**[▶ Drag the slider yourself](https://nonojamjam.github.io/noise-robust-detection-rkd/)** · **[▶ Click a target and let forward kinematics accept or reject it](https://nonojamjam.github.io/#fk)**

---

### Papers

1. **J. Park**, H. Seo. *An LLM Wiki System for High-Consequence Domain Knowledge Organization: Initial Feasibility for Space Operations and Nuclear Engineering.* 3rd IAA Conference on AI for Space, Jeju, Aug 2026 — first author, oral. [paper](https://nonojamjam.github.io/assets/papers/IAA2026_Park_LLM_Wiki_System.pdf) · [slides](https://nonojamjam.github.io/assets/talks/IAA2026_Park_talk_slides.pdf)
2. **J. Park**, H. Seo. *A VLM Robot Manipulation Pipeline for Mitigating Physical Hallucination* (in Korean). Korea Society of Industrial Information Systems, Spring 2026 — first author, oral. [slides (Korean)](https://nonojamjam.github.io/assets/talks/KSIIS2026_Park_talk_slides_ko.pdf)
3. KCI journal paper, co-author — LLM-driven evolutionary search over algorithm space (2026). · Patent pending, co-inventor — direction control in LLM embedding space (2026).

### Code

- [`noise-robust-detection-rkd`](https://github.com/nonojamjam/noise-robust-detection-rkd) — the capstone: RKD loss, custom Ultralytics trainer, re-measured results with seed checks. What did not work is in the README too.
- [`nonojamjam.github.io`](https://github.com/nonojamjam/nonojamjam.github.io) — this portfolio, including the FK gate toy.

<sub>Earlier: eLoran time-of-arrival under random sample loss (NAVIS Lab, 1,000-run Monte-Carlo; plain accumulation won). Details in person.</sub>
