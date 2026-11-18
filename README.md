# Machine Learning 1 — Homework 3

Solutions to Homework 3 of Data 37711 (Machine Learning & AI, Part I), Fall 2026, by Erik Friedrich.

- **Problem 1:** boosting with regression trees for a Poisson model of count data: loss, gradient and how each tree is chosen.
- **Problem 2:** a generalization bound for selecting hyperparameters on a test set, why the same set shouldn't be used for selection and evaluation, and a train / validation / test grid search with `RandomForestRegressor` and `KNeighborsRegressor` on the white wine quality data.
- **Problem 3:** generalization of gradient boosting with 1 to 1000 trees on two datasets, and what property of the data explains the difference.

## Files

| File | Contents |
|---|---|
| `hw3_Friedrich_Erik.ipynb` | The full solution: code, outputs and answers |
| `hw3_Friedrich_Erik.pdf` | The same notebook as a PDF |
| `winequality-white.csv` | Data for Problem 2(c) |
| `dset0-1.csv`, `dset1-1.csv` | Data for Problem 3 (no header row; the first column is the binary label) |
| `pdf_template/` | LaTeX template for exporting the notebook to PDF |

## Running it

Requires Python 3.12. From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

# run the whole notebook and save the outputs in place
jupyter nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=-1 hw3_Friedrich_Erik.ipynb

# export it to PDF (needs a LaTeX installation with xelatex)
jupyter nbconvert --to pdf --template pdf_template hw3_Friedrich_Erik.ipynb
```

All paths are relative to the repository root, so the commands must be run from there. A run takes about 3 minutes on a laptop CPU, most of it for the random forest grid search.

All random seeds are fixed, so rerunning the notebook gives the same results (tested on an Apple Silicon Mac with the versions in `requirements.txt`).
