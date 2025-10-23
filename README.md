# CURACAO_EV – Electric Vehicle Adoption Model

This repository contains the exploratory modelling and scenario discovery analyses for the **electric vehicle (EV) transition in Curaçao JIP TU Delft Project 2025**.  
The work integrates a Vensim system dynamics model with the **EMA Workbench** for exploratory modelling, uncertainty analysis, and PRIM scenario discovery.

---

## Repository structure

```
CURACAO_EV/
│
├── figures/                      # Generated figures and plots
│
├── model_files/                  # Vensim models and input files
│   ├── Current.vdfx
│   ├── ev_curacao_model.mdl
│   └── ev_curacao_model.vpmx
│
├── results/                      # Saved experiment results (tar.gz files)
│   ├── results_NO_POLICY.tar.gz
│   └── results_PRIM_WITH_POLICY.tar.gz
│
├── final_experiments.ipynb       # Main analysis and experiments
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```

---

## ⚙️ Setup and environment

It is recommended to run this notebook in an isolated virtual environment.

### 1. Create and activate a virtual environment
```bash
# Create venv
python -m venv .venv

# Activate
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

> Some dependencies (e.g. `ema_workbench`, `VensimModel`) require a **local Vensim installation** and valid license to run the model interface.

---

## 🚀 Usage

1. Open the main notebook:
   ```bash
   jupyter lab
   ```
   or open `final_experiments.ipynb` in **VS Code**.

2. Set the working directory to the project root so that paths like `./model_files/` and `./results/` resolve correctly.

3. Run the notebook cells sequentially to:
   - Load the Vensim model from `model_files/`
   - Run experiments under various policy and uncertainty settings
   - Save outputs to the `results/` folder
   - Perform PRIM scenario discovery and generate plots under `figures/`

