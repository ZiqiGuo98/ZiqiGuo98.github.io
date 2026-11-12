---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

Hi, I'm Dr. Ziqi Guo, a Machine Learning Researcher at **Apple** working on battery modeling and simulation. My work sits at the intersection of **AI for Science, multiscale physics modeling, and high-performance computing**: I build physics-informed machine learning models and LLM-agent workflows that turn slow, expensive simulations and manual engineering processes into fast, reliable tools for energy, thermal management, and sustainability.

I received my Ph.D. in Mechanical Engineering from Purdue University (Aug. 2025, GPA 3.97/4.00), co-advised by Prof. [Xiulin Ruan](https://engineering.purdue.edu/NANOENERGY/) and Prof. [Guang Lin](https://www.math.purdue.edu/~lin491/). Before that, I earned my B.E. with Honors in Energy & Power Engineering from Huazhong University of Science and Technology (rank 1/221, GPA 3.99/4.00).

## Current work

**Machine Learning Researcher, Battery Modeling & Simulation, Apple (Jun. 2025 – present)**

- Developed a **physics-informed ML framework** that combines physics priors with a fine-tuned transformer-based tabular foundation model to predict the performance of new battery cell designs across form factors, with **30% lower error** than the empirical scaling rules used previously.
- Applied the framework to a next-generation cell chemistry ahead of hardware builds (predictions within 15% of measurements), and combined it with physics-based open-circuit-voltage, impedance, and aging models calibrated to cell test data to evaluate control algorithms and design feasibility across three product lines.
- Built an **end-to-end LLM agent pipeline** that extracts and validates inputs from design documents and cell test data, runs the ML framework to generate full cell models, and drafts reports that flag risks, **cutting turnaround from one week to one day**.
- *Research intern (May – Aug. 2024):* developed numerical solvers for an on-device physics-based lithium-ion battery model (**16× faster simulation**) and a time-series model for on-device user-behavior forecasting (**50% higher accuracy** than the existing model).

## Research background

During my Ph.D. I developed ML and HPC methods that accelerate first-principles simulation of how heat and light move through materials.

- **Fast phonon transport.** Built an ML model that predicts phonon scattering rates and lattice thermal conductivity at first-principles accuracy with up to **100× speedup**, and a statistical-sampling method that makes converged calculations tractable. Then built **FourPhonon_GPU**, a CPU–GPU heterogeneous scheme (MPI/OpenMP + OpenACC) that gives up to 26× overall speedup (400× for the four-phonon scattering step). All are released in the open-source [FourPhonon](/open_source_code/1_FourPhonon) package and were featured twice by Purdue Engineering.
- **Atomistic foundation models.** Fine-tuned a pretrained universal ML force field for Al/Si interfaces, reaching *ab initio* accuracy (RMSE < 0.8 meV/atom) with ~100× faster molecular dynamics.
- **Physics-informed neural networks.** Developed PINNs for forward and inverse heat transfer, recovering thermal diffusivity from sparse temperature data with < 5% relative error.
- **Radiative cooling and optics.** Co-developed the open-source [FOS](/open_source_code/2_FOS) Monte Carlo photon-transport solver, built an RNN surrogate that is **700× faster** than Monte Carlo for multi-layer media (< 1% error), and designed a generative inverse-design pipeline that nearly doubles the visible reflectance of colored radiative cooling paints (40% → 76% at matched color).
- **Materials physics.** First-principles studies of hexagonal boron nitride (thermal conductivity, Raman/IR linewidths) and its use as a radiative cooling pigment, and of β-Ga2O3 thermal transport.

In total I have published 20+ papers (see [Publications](/publications/) or my [Google Scholar](https://scholar.google.com/citations?user=CJBGkTwAAAAJ&hl=en) profile), with 560+ citations and an h-index of 12.

## Skills

- **Machine learning:** physics-informed ML, ML force fields, graph and recurrent neural networks, surrogate modeling, inverse design, time-series forecasting, foundation-model fine-tuning (PyTorch, TensorFlow, scikit-learn)
- **LLM agents:** information extraction, workflow automation (LangChain, LangGraph, Claude Agent SDK)
- **Physics modeling:** battery equivalent-circuit and aging models, DFT, molecular dynamics, finite element analysis
- **Programming & HPC:** Python, C/C++, Fortran, MATLAB, SQL; MPI, OpenMP, OpenACC, CUDA, SLURM

## Selected honors

- **Dimitris N. Chorafas Foundation Award** (2025): about 20 doctoral recipients worldwide
- **Graduate Student Gold Award**, Materials Research Society (2025): MRS's highest graduate student honor
- **Magoon Research Excellence Award**, Purdue University (2025): four recipients per year
- **Warren and Judy Stevenson Scholarship** for outstanding research in applied optics (2024)
- **Best / Outstanding Presentation Awards** at ASME conferences (3×, 2023–2024)
- National Scholarship (3×) and Exemplary Merit Student Award, HUST

More in [News](/News/).

## Recent news

{% assign recent_news = site.News | reverse %}
{% for post in recent_news limit:3 %}
* [{{ post.title }}]({{ base_path }}{{ post.url }})
{% endfor %}

[See all news]({{ base_path }}/News/)

## Selected publications

{% for pub in site.data.publications %}{% if pub.selected %}
* {{ pub.citation }}{% if pub.link %} [Link]({{ pub.link }}){% endif %}{% if pub.pdf %}, [Paper]({{ pub.pdf }}){% endif %}
{% endif %}{% endfor %}

[Full publication list]({{ base_path }}/publications/)
