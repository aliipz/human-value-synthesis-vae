# Dynamic Synthesis of Human Value Profiles via Variational Autoencoders

[![Paper](https://img.shields.io/badge/Paper-VALE@IJCAI2026-blue)]()
[![Python](https://img.shields.io/badge/Python-3.9+-green)]()
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aliipz/human-value-synthesis-vae/blob/main/VAE_human_values.ipynb)
[![License](https://img.shields.io/badge/License-MIT-yellow)]()

This repository contains the code for the paper **"Dynamic Synthesis of Human Value Profiles via Variational Autoencoders"**, presented at the **VALE Workshop @ IJCAI-ECAI 2026**.

## Overview

We propose a Variational Autoencoder (VAE) framework for the dynamic synthesis of human value profiles grounded in **Schwartz's Theory of Basic Human Values**. Trained on the European Social Survey (ESS Round 11), the model learns a continuous, structured latent representation that captures the correlational topology of the Schwartz circumplex — without any explicit structural supervision.

## Key Capabilities

- **Synthetic population generation**: Generate large populations of psychologically coherent value profiles by sampling from the learned latent space
- **Latent space interpolation**: Smooth, psychologically coherent transitions between divergent value archetypes
- **Targeted sampling**: Oversample rare or underrepresented value profiles by perturbing specific latent coordinates

## Results

| Metric | Value |
|--------|-------|
| KS Similarity (avg, 1 − D_KS) | 0.928 |
| MMD (RBF kernel) | 0.010 |
| α-Precision | 0.997 |
| β-Recall | 0.590 |
| Pearson correlation similarity | 0.974 |
| TSTR utility retention | 95.8% |

## Data

This project uses the **European Social Survey Round 11** (ESS11). The dataset requires free registration and can be downloaded from:

👉 [https://ess.sikt.no/en/series/321b06ad-1b98-4b7d-93ad-ca8a24e8788a](https://ess.sikt.no/en/series/321b06ad-1b98-4b7d-93ad-ca8a24e8788a)

See `data/README_data.md` for detailed download and setup instructions.

## Usage

### Google Colab (recommended)

Click the badge at the top to open the notebook directly in Colab. All required libraries are pre-installed in the Colab environment. Upload the ESS dataset to your session before running.

### Local

Open and run `VAE_human_values.ipynb`. The notebook auto-detects the environment and sets paths accordingly. All standard scientific Python libraries are required (torch, numpy, pandas, scikit-learn, scipy, matplotlib, seaborn).

The notebook is structured as follows:

1. **Data loading and preprocessing** — PVQ-21 aggregation, ipsatization, standard scaling
2. **VAE architecture and training** — β-annealing strategy, latent bottleneck k=5
3. **Latent space analysis** — PCA projection revealing Schwartz's canonical axes
4. **Interpolation** — smooth trajectories between psychological archetypes
5. **Targeted sampling** — local sampling around rare empirical profiles
6. **Statistical validation** — KS, MMD, α-Precision, β-Recall, Pearson similarity, TSTR

## Project Structure

```
├── VAE_human_values.ipynb       # Main notebook (Colab-compatible)
├── data/
│   └── README_data.md           # Instructions to download ESS data
└── README.md
```

## Citation

If you use this code, please cite:

```bibtex
@inproceedings{pina2026dynamic,
  title     = {Dynamic Synthesis of Human Value Profiles via Variational Autoencoders},
  author    = {Pina Zapata, Alicia and Billhardt, Holger and Ossowski, Sascha},
  booktitle = {VALE Workshop @ IJCAI-ECAI 2026},
  year      = {2026}
}
```

## Acknowledgments

This work is supported by project grant EVASAI: PID2024-158227NB-C32 funded by MICIU/AEI/10.13039/501100011033/ FEDER, UE, and by grant COSASS: PID2021-123673OB-C32 funded by MCIN/AEI/10.13039/501100011033, by "ERDF A way of making Europe".

## License

MIT License
