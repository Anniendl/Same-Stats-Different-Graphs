# Same-Stats-Different-Graphs
# Same Stats, Different Graphs: Simulated Annealing for Dataset Generation

**Defence Institute of Advanced Technology (DIAT), Pune**  
**Course:** AM609L Data Science Tools & Techniques (DSTT) Lab (Autumn 2026)  
**Group:** 6  

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Pure_Implementation-deepgreen.svg)](https://numpy.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

## Project Overview
This repository contains the implementation of the "Same Stats, Different Graphs" phenomenon, originally popularized by F.J. Anscombe in 1973 and generalized by Justin Matejka and George Fitzmaurice (CHI 2017). 

The core objective of this project is to demonstrate that datasets sharing identical summary statistics (mean, variance, and Pearson correlation up to two decimal places) can exhibit vastly different spatial distributions. We achieve this by developing a custom stochastic optimization algorithm (Simulated Annealing) from scratch using pure NumPy, perturbing a seed dataset into predefined geometric target shapes while strictly enforcing mathematical invariants.

## Repository Structure
```text
Same-Stats-Different-Graphs/
├── .gitignore
├── README.md
├── Data/
│   └── Cleaned_Data/
│       ├── anscombe.csv              # Baseline Anscombe's Quartet
│       ├── datasaurus.csv            # The Datasaurus Dozen subsets
│       └── seed_data/                # Initial starting points for annealing
├── Notebook/
│   ├── 01_data_cleaning_sourabh.ipynb
│   ├── 02_baseline_stats_ritik.ipynb
│   ├── 03_simulated_annealing_aniruddha.ipynb (In Progress)
│   └── 04_master_pipeline.ipynb               (Pending)
└── Report_and_Admin/
    ├── AM609L_Project_Report.pdf              (Pending)
    ├── Seminar_Presentation.pptx              (Pending)
    └── Figures/                               # High-res vector plots
