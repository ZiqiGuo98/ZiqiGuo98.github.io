---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

Hi, I'm Dr. Ziqi Guo, a **Machine Learning Researcher at Apple**. I use AI to make physics simulation faster and engineering design smarter. My applications span **batteries** (predicting the performance of new cell designs), **thermal management and heat transfer** (phonon and thermal-conductivity simulation), **radiative cooling and optics** (nanoparticle paints and infrared properties), and **semiconductor and electronic materials** (hBN, β-Ga2O3, and Al/Si interfaces). The methods behind them are physics-informed ML, surrogate modeling, foundation-model fine-tuning, and GPU computing. I also build LLM agents and agent memory systems that automate the manual engineering workflows around them.

I received my Ph.D. in Mechanical Engineering from Purdue University (2025), co-advised by Prof. [Xiulin Ruan](https://engineering.purdue.edu/NANOENERGY/) and Prof. [Guang Lin](https://www.math.purdue.edu/~lin491/). Before that, I earned my B.E. with Honors from Huazhong University of Science and Technology.

## What I work on

### AI for scientific simulation and design

- **Foundation models for battery design.** At Apple, I use a fine-tuned foundation model with physics priors in place of empirical rules to understand battery design and physics, cutting prediction error by 30% and predicting new cell designs before hardware is built.
- **Accelerating thermal and optical simulation.** I combined machine learning, statistical sampling, and GPU computing to speed up first-principles thermal transport (phonon) calculations and photon Monte Carlo optical simulations by 100× and more, and released the results as open-source codes: [FourPhonon](/open_source_code/1_FourPhonon) for thermal transport and [FOS](/open_source_code/2_FOS) for optical spectra.
- **Generating new material designs.** I built surrogate-driven generative inverse design to find new material formulations, for example colored radiative cooling paints with nearly double the visible reflectance at matched color.

### Atomistic-scale simulation and foundation models

- I study materials at the atomistic scale with first-principles simulation and the AI-for-materials paradigm, including fine-tuning pretrained atomistic foundation models (universal ML force fields) to get *ab initio* accuracy at a fraction of the cost.

### Agentic AI

- I build LLM agents that fully automate performance prediction for new battery cell designs, cutting a one-week manual workflow to one day.
- I build agent memory systems for team applications: hybrid retrieval (RAG), knowledge graphs, and persistent shared memory that let agents recall, update, and reuse team knowledge across tasks.

In total I have published 20+ papers (see [Publications](/publications/) or my [Google Scholar](https://scholar.google.com/citations?user=CJBGkTwAAAAJ&hl=en) profile), with 560+ citations and an h-index of 12. My work has been recognized with several [awards and honors](/awards/).
