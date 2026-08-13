# Ridge Regression on the UCI Communities and Crime Dataset

> A reproducible notebook that applies ridge regression to the UCI Communities and Crime dataset and evaluates regularized linear prediction of violent crime per population.

## Overview

A reproducible notebook that applies ridge regression to the UCI Communities and Crime dataset and evaluates regularized linear prediction of violent crime per population. This repository preserves the implementation, source data or supporting artifacts, and the original project outputs so the work can be reviewed and reproduced.

## Motivation

Crime data contains many correlated socioeconomic predictors. Ridge regression provides a practical way to control coefficient magnitude while retaining all features in a high-dimensional linear model.

## Goal and Research Question

**Goal:** Prepare the Communities and Crime data, train a ridge model, and compare training and held-out performance.

**Question:** How effectively can an L2-regularized linear model predict violent crime per population from the available community attributes?

## Technical Approach

1. Load the unnormalized Communities and Crime data with pandas.
2. Select numeric predictors and the ViolentCrimesPerPop target.
3. Create a reproducible train/test split with random_state=0.
4. Fit Ridge(alpha=200.0).
5. Report intercept, coefficients, non-zero feature count, and R² scores.

## Tech Stack

| Technology | Role |
|---|---|
| Python | Analysis environment |
| pandas | Data loading and preparation |
| NumPy | Numerical operations |
| scikit-learn | Train/test split and ridge regression |
| Jupyter Notebook | Executable analysis narrative |

## Results and Deliverables

- The notebook processes 1,994 community records.
- With alpha=200.0, the recorded training R² is 0.669 and test R² is 0.488.
- The fitted model retains 88 non-zero features.
- These values are saved notebook outputs and should be rechecked after dependency or preprocessing changes.

## Repository Contents

| Path | Purpose |
|---|---|
| `Ridge Regression Using UCI Dataset.ipynb` | Source analysis |
| `CommViolPredUnnormalizedData.txt` | Communities and Crime data |
| `Ridge Regression Using UCI Dataset.pdf` | Static notebook export |

## Getting Started

Clone the repository:

```bash
git clone https://github.com/CS-Ponkoj/Ridge-Regression-Using-UCI-Dataset.git
cd Ridge-Regression-Using-UCI-Dataset
```

### Requirements

```bash
python -m pip install pandas numpy scikit-learn jupyter
```

### Run or Review

```bash
jupyter notebook "Ridge Regression Using UCI Dataset.ipynb"
```

## Reproducibility Notes

- Results above come from code, saved notebook outputs, or artifacts currently stored in this repository.
- Paths from the original development environment may need to be changed to repository-relative paths.
- Re-run the work after dependency changes before comparing new outputs with the recorded values.

## Limitations and Next Steps

- The notebook contains an original local Windows path; replace it with the repository-relative data filename.
- R² indicates only moderate held-out fit, so results should not be used for operational decisions.
- Future work can add scaling, cross-validation, alpha selection, residual analysis, and fairness checks.

## Author

**Ponkoj Shill**  
AI/ML researcher and Ph.D. candidate in Computer Science

- [GitHub](https://github.com/CS-Ponkoj)
- [Portfolio](https://ponkoj.com)

## License

No license file is currently included. Please contact the author before reusing the project beyond review, education, or fair-use evaluation.
