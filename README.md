## Juhyeok Park · 박주혁

**Electronic Engineering, Chungbuk National University · B.S. Feb 2027 · applying for Spring 2027 graduate programs in Physical AI**

> Language models work from descriptions of physical tasks. Three undergraduate projects: an LLM wiki with ambient context
> injection, a VLM manipulation pipeline with forward-kinematics verification, a noise-robust detector with heterogeneous
> relational distillation. The LLM given the right document — hallucination. The VLM given the right joint angles — 277 mm
> position error. The detector trained on noisy images — robustness. Research goal: a model whose input includes physical
> and multimodal measurements.

🌐 **[Portfolio — numbers, demos, papers →](https://nonojamjam.github.io/)** · 📄 **[CV (PDF)](https://nonojamjam.github.io/assets/cv/CV_JuhyeokPark_2026-09.pdf)**

---

### Three studies, one limitation

| | Measurement | Finding |
|---|---|---|
| **01 · Noise-robust satellite detection** (capstone, sole ML/code) | Noisy mAP50 **+0.163** (σ=0.3, seed-stable); clean **−0.053** | 97% of the gain is attributable to training on the corrupted signal; distillation adds +0.005 |
| **02 · An LLM that writes and reads its own wiki** (KAERI · IAA 2026, first author) | **94%** blind agreement between two cross-family graders | Hallucination persisted with the correct node injected directly; knowledge access is not the limiting factor |
| **03 · VLM robot commands gated by forward kinematics** (KAERI · KSIIS 2026, first author) | Position error **165.7 → 276.9 mm** when the VLM was *given* joint angles | Language does not carry the physical quantities the task requires; verification must be external to the model |

Method, limitations and interactive material: [portfolio](https://nonojamjam.github.io/#capstone).

### Two further threads (KAERI, 2026)

| | Role | Content |
|---|---|---|
| **AI agent framework for autonomous improvement of an ultrasonic (SAFT) imaging algorithm** — *J. Korean Soc. Nondestruct. Test.* 46(4), 2026 (KCI) | co-author | An LLM agent iteratively edits the SAFT code; an evaluator scores each edit and keeps improvements. Six defect conditions; three design variables tested. Findings: per-item scoring > total score; **one edit per iteration > several** (the LLM cannot attribute cause with many edits); **no edit history → std 0**, the search collapses (ANOVA p < 0.001); the 1 mm defect below the 3.16 mm wavelength never improved — a diffraction limit that code optimisation cannot move. Contribution: benchmark task design and code documentation. [DOI](https://doi.org/10.7779/JKSNT.2026.46.4.268) |
| **Idea Compass** — patent pending, 2026 | co-inventor | Coarse directional steering of LLM idea generation in embedding space, with a human-in-the-loop gauge. Presented as the steering component of the IAA wiki system; the internal mechanism is not disclosed pending the filing. |

Both concern *what an LLM can produce* when placed inside a search or steering loop — the complementary question to the three studies above, which concern *what it cannot execute*.

---

### Interactive material

[![Same noisy satellite tile: baseline finds nothing, the noise-trained model keeps the lock](https://nonojamjam.github.io/assets/profile/noise_slider.gif)](https://nonojamjam.github.io/noise-robust-detection-rkd/)

**[▶ Noise slider — baseline vs. proposed detector](https://nonojamjam.github.io/noise-robust-detection-rkd/)** · **[▶ Forward-kinematics gate — propose a target, observe accept/reject](https://nonojamjam.github.io/#fk)**

---

### Papers

1. **J. Park**, H. Seo. *An LLM Wiki System for High-Consequence Domain Knowledge Organization: Initial Feasibility for Space Operations and Nuclear Engineering.* 3rd IAA Conference on AI for Space, Jeju, Aug 2026 — first author, oral. [paper](https://nonojamjam.github.io/assets/papers/IAA2026_Park_LLM_Wiki_System.pdf) · [slides](https://nonojamjam.github.io/assets/talks/IAA2026_Park_talk_slides.pdf)
2. **J. Park**, H. Seo. *A VLM Robot Manipulation Pipeline for Mitigating Physical Hallucination* (in Korean). Korea Society of Industrial Information Systems, Spring 2026 — first author, oral. [slides (Korean)](https://nonojamjam.github.io/assets/talks/KSIIS2026_Park_talk_slides_ko.pdf)
3. D. Choi, **J. Park**, H. Seo, “Development of an AI Agent Framework for Autonomous Improvement of an Ultrasonic Imaging Algorithm,” *J. Korean Soc. Nondestruct. Test.* 46(4):268–277, 2026 (KCI, co-author). · Patent pending, co-inventor — Idea Compass, directional steering in LLM embedding space (2026).

### Code

- [`noise-robust-detection-rkd`](https://github.com/nonojamjam/noise-robust-detection-rkd) — capstone: RKD loss, custom Ultralytics trainer, re-measured results with seed checks. Negative results are documented in the README.
- [`nonojamjam.github.io`](https://github.com/nonojamjam/nonojamjam.github.io) — this portfolio, including the forward-kinematics illustration.

<sub>Earlier: eLoran time-of-arrival under random sample loss (NAVIS Lab, 1,000-run Monte-Carlo; plain accumulation outperformed both compensation schemes). Details available on request.</sub>
