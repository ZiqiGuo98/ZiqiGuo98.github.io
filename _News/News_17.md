---
title: "FourPhonon_GPU published in Cell Reports Physical Science"
excerpt: "CPU-GPU heterogeneous computing for phonon scattering and thermal conductivity."
collection: News
---

Our paper **"FourPhonon_GPU, a CPU-GPU heterogeneous computing scheme for phonon scattering and thermal conductivity calculations"** is published in *Cell Reports Physical Science* (2026). The scheme offloads scattering-rate calculations with OpenACC and resolves warp divergence through CPU-side process filtering, achieving up to **26x overall speedup** (and 400x for the four-phonon scattering-rate step) under the relaxation-time approximation. It and is released in the open-source [FourPhonon](/open_source_code/1_FourPhonon) package (v1.3).

- Paper: [Cell Reports Physical Science](https://doi.org/10.1016/j.xcrp.2026.103491) · [arXiv](https://arxiv.org/abs/2510.00518)
- Media: [FourPhonon simulations now 26 times faster with GPU acceleration](https://engineering.purdue.edu/ME/News/2026/fourphonon-simulations-now-26-times-faster-with-gpu-acceleration) (Purdue Mechanical Engineering)
