# iMEDSoS — Layered Systems-of-Systems Intelligence for Healthcare

> **Layered Systems-of-Systems Intelligence for Healthcare: Context-Aware Sensing,
> Privacy-Sharded Blockchain Security, and ListenFirst Federated Learning
> in a Unified Edge–Cloud Architecture**
>
> Akoramurthy B · Surendiran B · Xiaochun Cheng · Sathishkumar VE · Sachi Nandan Mohanty

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![LaTeX](https://img.shields.io/badge/LaTeX-manuscript-green.svg)]()

---

## Repository Structure

```
iMEDSoS-Nexus/
├── main/                          # Main manuscript
│   ├── iMEDSoS_Nexus_Main.tex    # Complete main manuscript (final version)
│   └── references.bib            # Bibliography
│
├── supplementary/                 # Supplemental Information
│   ├── Supplementary_Complete.tex # Full supplemental file (Algs S1–S4,
│   │                              #   Tables S1–S4, Figs S1–S6 captions)
│   └── Supplementary_Algorithms.tex  # Algorithms S1–S4 standalone
│
├── figures/
│   ├── main_figures/              
│   ├── dataset3_figures/          # Dataset 3 result figures
│   │   ├── Fig_D3_PerClass_Performance.png
│   │   ├── Fig_D3_ConfusionMatrix.png
│   │   ├── Fig_D3_LFMLConvergence.png
│   │   ├── Fig_D3_ModalityAblation.png
│   │   ├── Fig_D3_NodeContribution_Fixed.png
│   │   ├── Fig_D3_ThresholdSensitivity.png
│   │   ├── Fig_D3_BaselineComparison.png
│   │   └── Fig_D3_ROC_Curves.png
│   └── supplemental_figures/     # Supplemental figures S1–S5 
│       ├── Fig_S1_Scalability_Extended.png
│       ├── Fig_S2_CASPA_k1k2_sweep.png
│       ├── Fig_S3_CASPA_k3k4_sweep.png
│       ├── Fig_S4_LFML_Convergence_HCC_CKD.png
│       └── Fig_S5_APS_Weight_Heatmap.png
│
├── tables/                        # Standalone table snippets
│   ├── table_multimodal_landscape.tex   # Tab. 5 — 8-col, landscape fix
│   └── tables_ablation_nodes.tex        # Tab. 6–7 — ablation & node tables
│
├── scripts/                       # Python figure-generation scripts
│   ├── plot_dataset3_figures.py   # Generates all Dataset 3 result figures
│   └── plot_supplemental_figures.py  # Generates Figs S1–S5
│
├── .gitignore
└── LICENSE
```

---

## Compilation

### Main manuscript
```bash
cd main
pdflatex iMEDSoS_Nexus_Main.tex
bibtex   iMEDSoS_Nexus_Main
pdflatex iMEDSoS_Nexus_Main.tex
pdflatex iMEDSoS_Nexus_Main.tex
```

### Supplementary file
```bash
cd supplementary
pdflatex Supplementary_Complete.tex
bibtex   Supplementary_Complete
pdflatex Supplementary_Complete.tex
pdflatex Supplementary_Complete.tex
```

### Regenerate all figures
```bash
pip install matplotlib numpy seaborn scipy
python scripts/plot_dataset3_figures.py
python scripts/plot_supplemental_figures.py
```
Figures are saved to `figures/dataset3_figures/` and `figures/supplemental_figures/`.

---

## Key Contributions

| Contribution | Description |
|---|---|
| **ListenFirst ML (LFML)** | Relevance-weighted federated aggregation with formal convergence proof |
| **Adaptive Privacy Sharding (APS)** | HIPAA-calibrated 4-component sensitivity scoring, AES-256/AES-128/ChaCha20 tiering |
| **Four-layer SoS Architecture** | CAS → DDPL → CIL → BSL under a unified multi-objective optimization |
| **Three-dataset validation** | HCC (88% acc), CKD (98.5% acc), QAI-MEdge multimodal (95.3% acc) |

---

## Datasets

| Dataset | Source | Task |
|---|---|---|
| HCC (Hepatocellular Carcinoma) | [UCI ML Repository](https://archive.ics.uci.edu) | Binary survival prediction |
| CKD (Chronic Kidney Disease) | [UCI ML Repository](https://archive.ics.uci.edu) | Binary classification |
| QAI-MEdge Layer 1 (Multi-Modal Biosignal) | [Mendeley Data](https://doi.org/10.17632/rff4-4r66-26) | 5-class cardiac classification |

---

## Requirements

- **LaTeX**: TeX Live 2022+ or MikTeX; packages: `booktabs`, `algorithm`, `algpseudocode`, `amsmath`, `threeparttable`, `pdflscape`, `mdframed`, `enumitem`, `siunitx`, `cleveref`
- **Python**: 3.9+; `matplotlib`, `numpy`, `seaborn`, `scipy`
- **Testbed**: Raspberry Pi 4B (4 GB RAM, TF Lite 2.11) + AWS EC2 t3.medium + Hyperledger Fabric 2.4

---

## Citation

```bibtex
@article{akoramurthy2025imedsos,
  title   = {Layered Systems-of-Systems Intelligence for Healthcare:
             Context-Aware Sensing, Privacy-Sharded Blockchain Security,
             and {ListenFirst} Federated Learning in a Unified
             Edge--Cloud Architecture},
  author  = {Akoramurthy, B and Surendiran, B and Cheng, Xiaochun
             and Sathishkumar, VE and Mohanty, Sachi Nandan},
  journal = {[Under Review]},
  year    = {2025}
}
```

---

## Correspondence

- **Lead contact**: Akoramurthy B — [cs22d1005@nitpy.ac.in](mailto:cs22d1005@nitpy.ac.in)
- **Supervisor**: Surendiran B — [surendiran@nitpy.ac.in](mailto:surendiran@nitpy.ac.in)
- National Institute of Technology Puducherry, Karaikal, India

---

## License

This repository is released under the [MIT License](LICENSE).
