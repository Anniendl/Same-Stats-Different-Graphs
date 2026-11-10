<div align="center">
  <h1>🦖 Same Stats, Different Graphs</h1>
  <h3>Geometric Morphing via Simulated Annealing under Strict Statistical Constraints</h3>
  
  [![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
  [![NumPy](https://img.shields.io/badge/NumPy-Pure-green.svg)](https://numpy.org/)
  [![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()
  
  <p><i>An M.Tech Data Science Implementation highlighting the critical necessity of spatial visualization in statistical analysis.</i></p>
</div>

---

## 📌 The Premise

Summary statistics (Mean, Variance, Pearson Correlation) are foundational to data science, but they possess a critical blind spot: radically divergent spatial geometries can share identical statistical signatures. 

Inspired by **Anscombe’s Quartet** and the **Datasaurus Dozen**, this project transitions from baseline statistical proofs to advanced stochastic optimization. We engineered a Simulated Annealing algorithm capable of morphing a starting point cloud (`dino`) into a target geometry (`star`), while actively restricting statistical drift to a microscopic tolerance window. 

Evaluators relying solely on summary statistics would be mathematically unable to distinguish the original dinosaur point cloud from the morphed star geometry.

---

## ⚖️ Academic Constraints & Engineering Choices

To ensure rigorous proof of work and adhere to strict evaluation criteria, this repository was built under the following constraints:

1. **Pure NumPy Architecture:** High-level, "black-box" statistical libraries (e.g., `SciPy`, `scikit-learn`) were strictly prohibited. All metrics—Mean, Sample Variance, Pearson $r$, and Ordinary Least Squares (OLS) regression—were manually engineered using pure `numpy` arrays.
2. **Transparent Execution (No Automated Looping):** To provide an auditable, transparent proof of mathematical logic, automated `for` loops were abandoned during the baseline validation phases. The datasets were processed explicitly, cell-by-cell, highlighting the raw computational labor and exposing the intermediate steps of the mathematical proofs.
3. **Strict Separation of Concerns:** Extract, Transform, Load (ETL) operations are strictly siloed from downstream statistical processing to maintain professional software architecture standards.

---

## 🗂️ Repository Architecture

The project is structured sequentially across four primary Jupyter Notebooks:

```text
📦 Same-Stats-Different-Graphs
 ┣ 📂 Data
 ┃ ┣ 📜 anscombe_clean.csv
 ┃ ┗ 📜 datasaurus_clean.csv
 ┣ 📂 Notebook
 ┃ ┣ 📜 01_data_cleaning_sourabh.ipynb       # Phase 1: ETL Pipeline & Float64 Casting
 ┃ ┣ 📜 02_anscombe_stats_ritik.ipynb        # Phase 2a: Anscombe's Quartet Baseline
 ┃ ┣ 📜 03_datasaurus_stats_processing.ipynb # Phase 2b: Datasaurus Dozen Validation
 ┃ ┗ 📜 04_simulated_annealing.ipynb         # Phase 3: Stochastic Optimization Engine
 ┣ 📂 Assets
 ┃ ┣ 🖼️ anscombe.png
 ┃ ┣ 🖼️ dino.png
 ┃ ┗ 🖼️ star_sa.png
 ┗ 📜 README.md
```
⚙️ The Mathematical Engine: Simulated Annealing. The core of Phase 3 is a stochastic optimization algorithm designed to manipulate coordinates without triggering statistical alarms.1. The Gatekeeper (Statistical Constraint): A random coordinate is selected and perturbed via Gaussian noise. The modified dataset is immediately processed through the custom NumPy functions. If the new variance or correlation deviates from the original dino baseline by a tolerance greater than 0.1, the move is instantly rejected.2. The Objective Function (Spatial Cost)If the perturbation passes the statistical gatekeeper, its Euclidean distance to the target star geometry is calculated. Moves that decrease this cost are accepted. To prevent the points from becoming trapped in local minima, moves that increase the cost are accepted probabilistically based on the current system temperature $T$, defined by the formula: $P = e^{(-\Delta \text{Cost} / T)}$. Engine Performance Metrics: Iterations Executed: 150,000Cooling Rate: 0.9995Initial Spatial Cost: 1103.80Final Spatial Cost: 216.86Result: Achieved an 80.35% reduction in spatial divergence while perfectly preserving the dataset's statistical signature.📊 Visual Proof(Insert high-resolution comparative plots here displaying the original dino geometry vs. the morphed SA star geometry). Note on Geometric "Noise": The slight geometric scattering observed in the final star shape is the direct physical manifestation of the strict mathematical constraints holding the variance and correlation steady. The algorithm found the absolute closest physical approximation of a star that mathematically still acts like a dinosaur.👥 Team & Contributions: Aniruddha (Lead): Architecture Design & Simulated Annealing Engine Optimization; Sourabh: ETL Pipeline & Data Sanitization; Ritik: Pure NumPy Baseline Mathematical Equations; Astha: Documentation, Visualization, and Reporting Framework. 🚀 How to Run: Clone the repository: git clone https://github.com/Anniendl/Same-Stats-Different-Graphs.gitEnsure dependencies are installed: pip install numpy pandas matplotlib. Execute the notebooks sequentially from 01 to 04 to trace the data pipeline from raw ingestion to final geometric morphing.










