---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

Hi, I’m Dr. Ziqi Guo, a Machine Learning Researcher at Apple Inc., specializing in Scientific Machine Learning (SciML) and High-Performance Computing. My passion lies in accelerating scientific discovery by bridging the gap between rigorous engineering simulations and data-driven intelligence to solve critical challenges in energy, thermal management, and sustainability.

I obtained my Ph.D. degree in Mechanical Engineering at Purdue University, co-advised by Prof. [Xiulin Ruan](https://engineering.purdue.edu/NANOENERGY/) and Prof. [Guang Lin](https://www.math.purdue.edu/~lin491/).

I bring cross-functional collaboration skills and deep expertise in AI4Science and Scientific Computing, leveraging deep learning, predictive modeling, and large-scale simulations to solve complex engineering problems. My work integrates advanced deep learning architectures with high-performance computing (GPU acceleration) to bypass traditional bottlenecks, resulting in novel solutions for energy efficiency, battery modeling, and thermal management.

I have led initiatives to develop physics-informed machine learning (PIML) models that predict and optimize material properties by bridging the gap between quantum-mechanical calculations and macro-scale simulations. These efforts have directly advanced the capability to perform inverse design and optimization for battery, thermal, fluid, and optical systems.

I’ve also developed rigorous numerical solvers and two widely adopted open-source software packages, [FourPhonon v2.0](https://github.com/FourPhonon/FourPhonon) and [FOS](https://github.com/FastOpticalSpectrum/FOS), providing critical tools for the advancement of next-generation energy storage systems.

Key strengths include:

- AI-Driven Scientific Discovery: Expertise in utilizing Generative AI and Machine Learning to accelerate material discovery and achieve inverse design.
- High-Performance Computing: Advanced proficiency in parallel computing (MPI/OpenMP) and GPU acceleration (CUDA/OpenACC), reducing simulation times by 100x-10000x.
- Multiphysics Simulation: Proven ability to model thermal, fluid, optical, and battery systems using advanced numerical methods (MD, DFT, FEA).
- Domain Expertise in Energy Systems: Deep understanding of transport mechanisms, including phonon scattering and radiative cooling, applied to real-world engineering challenges.
- Research & Software Engineering: Demonstrated success in defining technical strategy, developing scalable open-source tools, and executing end-to-end research pipelines.

Recent News
------

{% assign recent_news = site.News | reverse %}
{% for post in recent_news limit:3 %}
* [{{ post.title }}]({{ base_path }}{{ post.url }})
{% endfor %}

[See all news]({{ base_path }}/News/)

Selected Publications
------

{% for pub in site.data.publications %}{% if pub.selected %}
* {{ pub.citation }} [Link]({{ pub.link }}), [Paper]({{ pub.pdf }})
{% endif %}{% endfor %}

[Full publication list]({{ base_path }}/publications/)
