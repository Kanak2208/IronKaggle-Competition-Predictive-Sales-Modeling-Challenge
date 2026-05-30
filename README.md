# IronKaggle - Predictive Sales Modeling Challenge

This repository contains a predictive modeling solution for the IronKaggle sales forecasting competition. The primary deliverable is a Jupyter notebook, `prediction_notebook.ipynb`, which demonstrates data loading, feature engineering, model training (LightGBM and XGBoost), ensembling, and generating submissions.

## Repository structure

- `prediction_notebook.ipynb` - end-to-end notebook: data exploration, feature engineering, model training, evaluation, and submission generation.
- `predictions.csv` - example output produced by the notebook (submission format).
- `README.md` - this file.

## Quickstart

1. Create and activate a Python environment (recommended):

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt  # or install packages listed below
```

2. Install core dependencies (if not using `requirements.txt`):

```bash
pip install pandas numpy scikit-learn matplotlib seaborn lightgbm xgboost
```

3. Run the notebook in VS Code or Jupyter:

```bash
jupyter lab  # or `jupyter notebook`
```

Open `prediction_notebook.ipynb` and run cells in order. The notebook downloads example data from a public URL, so no local data files are required to reproduce the end-to-end run.

## Notebook Overview

- Data loading and initial exploration
- Feature engineering (date features, store-level aggregations)
- Model training with LightGBM and XGBoost
- Ensemble predictions (simple average)
- Submission creation (`predictions.csv`)

## Output

The notebook saves final predictions to `predictions.csv` containing the `True_index` and predicted `Sales` values.

## Notes & Tips

- If you run into performance or compilation issues with `xgboost` on macOS, installing `libomp` (via Homebrew) can help:

```bash
brew install libomp
```

- For reproducible experiments, set random seeds in model constructors and data splits (the notebook uses `random_state=42`).

## Contact

For questions or collaboration, open an issue or contact the repository owner.
