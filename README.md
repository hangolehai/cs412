# CS 412 — Airbnb Price Prediction

Predicting Chicago Airbnb nightly prices and measuring how much location and amenity features improve Linear Regression, Random Forest, and XGBoost models.

## Layout

```
data/                  # Original dataset (listings.csv.gz, gitignored)
notebooks/             # Experiments
  CS412_Airbnb_Cursor_Ready.ipynb
results/               # Metrics and figures written by the notebook
reports/               # Intermediate and final reports
requirements.txt
README.md
.gitignore
```

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
brew install libomp    # macOS only, required by XGBoost
```

Place the Inside Airbnb detailed Chicago listings file at `data/listings.csv.gz`.

## Running

Open `notebooks/CS412_Airbnb_Cursor_Ready.ipynb`, select the `.venv` kernel, and run all cells. Or, from the project root:

```bash
.venv/bin/jupyter nbconvert --to notebook --execute --inplace notebooks/CS412_Airbnb_Cursor_Ready.ipynb
```

All tables and figures are written to `results/`.
