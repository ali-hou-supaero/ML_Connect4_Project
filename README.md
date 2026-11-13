# Connect Four — Supervised Outcome Classification

A machine-learning project by **Ali Houssenaly and Côme Guillarme**, studying the [UCI Connect-4 dataset](https://archive.ics.uci.edu/dataset/26/connect+4).

The objective is to predict **win, loss or draw for the first player** from a board position. This repository studies classification of labelled positions; it does not implement a complete game-playing agent.

## Approach

- Explore board states and class imbalance.
- One-hot encode board features and encode target labels when required.
- Compare Random Forest, SVM and XGBoost.
- Tune hyperparameters with GridSearchCV and compare raw-data and resampled approaches.
- Inspect confusion matrices and classification reports, with attention to macro F1 and minority classes.

The notebook contains the experimental discussion and saved outputs. Results have not been independently reproduced for this documentation update.

## Contents

- [Project notebook](HOUSSENALY_GUILLARME_Project.ipynb) — methodology, training/loading prompts and evaluation.
- [Video presentation](HOUSSENALY_GUILLARME_Video.mp4) — accompanying presentation.
- `models/` — saved Random Forest, SVM and XGBoost models, including resampled variants.

## Getting started

Install Git LFS before cloning. On Debian/Ubuntu:

```bash
sudo apt install git-lfs
git lfs install
git clone https://github.com/ali-hou-supaero/ML_Connect4_Project.git
cd ML_Connect4_Project
git lfs pull
```

On other operating systems, install Git LFS using the appropriate installer, then run `git lfs install` before cloning.

Use Jupyter with Python, ucimlrepo, pandas, NumPy, matplotlib, seaborn, scikit-learn, XGBoost and joblib. The notebook retrieves UCI dataset 26 using `fetch_ucirepo`, so network access is needed.

Launch the notebook from the repository root. When prompted, choose whether to train or load a model; loading the suggested saved model avoids repeating the grid search. Only load model files from sources you trust. Saved models can require the library versions used to create them; a pinned environment is not supplied.

## Reproducibility and credits

The analysis is a joint project. Model development, conclusions and presentation should be credited to both authors. Dataset provenance is the UCI link above. The repository preserves the original experiments and does not claim a newly validated benchmark.
