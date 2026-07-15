# Exponential Inequalities for Functional Data — Code

This repository contains the Python code (Jupyter notebooks) accompanying the paper
*"Some exponential inequalities for functional data: application to hypotheses testing in
Hilbert space"* (main paper and Supplementary Material, PDFs included below).

The paper derives a non-asymptotic exponential concentration inequality for the penalized
Hotelling's T² statistic in a separable Hilbert space, and applies it to one-sample and
two-sample hypothesis testing on functional (curve-valued) data. Each notebook reproduces
one or more figures/tables of the paper; file names indicate the corresponding figure
number(s).

## Repository structure

```
.
├── paper/    # PDFs of the main paper and Supplementary Material
└── code/     # Jupyter notebooks, one per figure (or group of figures)
```

## Notebook-to-figure mapping

| Notebook | Content | Reference in the paper |
|---|---|---|
| `FIGURE1_AND_FIGURE3.ipynb` | Simulated curves (Fourier basis), spectrum of Γₙ, and sensitivity of the test to the penalty α | Main paper, Figures 1 and 3 |
| `FIGURE2.ipynb` | Empirical power of the one-sample test (sign-flip permutation vs. theoretical bound) | Main paper, Figure 2 |
| `FIGURE4.ipynb` | Empirical power of the two-sample test | Main paper, Figure 4 |
| `FIGURE_7_9_11.ipynb` | Simulated curves and spectral structure for the Brownian motion (Fig. 7), Ornstein–Uhlenbeck (Fig. 9), and flat spectrum (Fig. 11) designs | Supplementary Material, §3 |
| `Supplementary_FIGURES_1_2.ipynb` | Two-sample homogeneity test (via the empirical cdf): mean shift and variance shift | Supplementary Material, Figures 1 and 2 |
| `Supplementary_FIGURES_3_4_5_6___TABLE_1.ipynb` | Real-data application to CICIDS2017 (network intrusion detection, BENIGN vs. DDoS) | Supplementary Material, Figures 3–6 and Table 1 |
| `Supplementary_FIGURES_8_10_12_pas_tourner.ipynb` | Empirical power of the one-sample test for the Brownian motion, Ornstein–Uhlenbeck, and flat spectrum designs | Supplementary Material, Figures 8, 10, and 12 |

## How to use

Each notebook is self-contained: open it and run the cells in order to reproduce the
corresponding figure. Simulation parameters (sample size n, grid resolution p, number of
Monte Carlo replications, penalty α, etc.) are set near the top of each notebook and can be
freely changed.

## Requirements

See [`requirements.txt`](requirements.txt). Install with:

```bash
pip install -r requirements.txt
```

**Notes:**
- Some notebooks (`FIGURE4`, `Supplementary_FIGURES_1_2`,
  `Supplementary_FIGURES_8_10_12_pas_tourner`) use `cupy` for GPU acceleration and were
  designed to run on Google Colab. They also run on CPU by simply replacing `cupy` with
  `numpy` in the import cell.
- `Supplementary_FIGURES_3_4_5_6___TABLE_1.ipynb` requires the
  [CICIDS2017](https://www.unb.ca/cic/datasets/ids-2017.html) dataset (files
  `Monday-WorkingHours.pcap_ISCX.csv` and `Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv`),
  not included here due to size; update the file paths near the top of the notebook.

## Citation

If you use this code, please cite the associated paper (see the PDFs in `paper/` for the
full reference list).

## License

Released under the MIT License (see [`LICENSE`](LICENSE)).
