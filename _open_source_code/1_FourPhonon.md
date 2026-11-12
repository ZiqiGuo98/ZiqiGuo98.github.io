---
title: "FourPhonon"
collection: open_source_code
permalink: /open_source_code/1_FourPhonon
excerpt: 'An extension module to ShengBTE for computing four-phonon scattering rates and lattice thermal conductivity, with ML, sampling, and GPU acceleration.<br/><img src="/images/FourPhonon-overview.png" width="500">'
---

<img src="/images/FourPhonon-overview.png" width="100%" alt="FourPhonon v1.0 to v2.0 overview">

**FourPhonon** is a Boltzmann transport equation (BTE) and phonon scattering solver built on the [ShengBTE](http://www.shengbte.org/) platform. It computes three- and four-phonon scattering rates in crystals, solves the linearized phonon BTE exactly, and outputs lattice thermal conductivity. The four-phonon formalism was developed by the [Ruan group](https://engineering.purdue.edu/NANOENERGY/) at Purdue.

**[GitHub repository](https://github.com/FourPhonon/FourPhonon)** · **[Manual](https://github.com/FourPhonon/FourPhonon/blob/main/Manual.md)** · License: GPL-3.0

## Why acceleration matters

Phonon scattering calculations are the computational bottleneck of first-principles thermal transport. Four-phonon processes are especially expensive, which makes high-throughput screening of thermal properties and large-system calculations difficult. My contributions to FourPhonon target this bottleneck from three directions.

## What I contributed

| Version | Feature | Reference |
|---|---|---|
| v1.1 | **Sampling acceleration**: statistical sampling of scattering processes gives converged scattering rates, thermal conductivity, and radiative properties at a fraction of the cost | [Guo et al., npj Comput. Mater. 10, 31 (2024)](https://www.nature.com/articles/s41524-024-01215-8) |
| (model) | **Machine learning prediction** of phonon scattering rates and thermal conductivity, up to ~100× faster at first-principles accuracy | [Guo et al., npj Comput. Mater. 9, 95 (2023)](https://www.nature.com/articles/s41524-023-01020-9) |
| v1.3 | **GPU acceleration** and **MPI + OpenMP hybrid scheme** (CPU–GPU heterogeneous computing with OpenACC): up to 26× overall speedup, 400× for the four-phonon scattering-rate step | [Guo et al., Cell Rep. Phys. Sci. 7 (2026)](https://doi.org/10.1016/j.xcrp.2026.103491) |

Other versions in the package: v1.0 (original software: Han, Yang, Li, Feng, Ruan) and v1.2 (iterative solver and TDEP force-constant interface: Han, Alkandari, Zhou, Ruan). The v2.0 overview figure above shows the full feature set: four-phonon iterative method, phonon renormalization, thermal radiative properties, statistical sampling, ML interatomic potentials, and GPU acceleration.

## Quick start

```bash
git clone https://github.com/FourPhonon/FourPhonon.git
cd FourPhonon/Src
# set compiler paths in arch.make, then:
make cpu     # builds ShengBTE_cpu
make gpu     # builds ShengBTE_gpu
```

See the manual for compiler settings and input files.

## Applications

High-temperature materials, chip cooling and thermal management, Raman and infrared spectroscopy (phonon linewidths), radiative properties, and energy storage materials.

## Citation

- Z. Han, X. Yang, W. Li, T. Feng, X. Ruan, [*FourPhonon: An extension module to ShengBTE for computing four-phonon scattering rates and thermal conductivity*](https://doi.org/10.1016/j.cpc.2021.108179), Comput. Phys. Commun. 270, 108179 (2022).
- For the acceleration features, please also cite the sampling, ML, and GPU papers listed above.

## Media

- [New machine learning method turbocharges heat transfer simulations](https://engineering.purdue.edu/ME/News/2024/new-machine-learning-method-turbocharges-heat-transfer-simulations), Purdue Mechanical Engineering
- [FourPhonon simulations now 26 times faster with GPU acceleration](https://engineering.purdue.edu/ME/News/2026/fourphonon-simulations-now-26-times-faster-with-gpu-acceleration), Purdue Mechanical Engineering

*Supported by the NSF CSSI Elements program (award #2311848).*
