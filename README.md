# CART Classifier from Scratch (DATA2060 Final Project) -- The Overfitters

Implementation of a CART (Classification and Regression Tree) classifier built with only Python and NumPy, plus a full test suite comparing our model to `sklearn.tree.DecisionTreeClassifier`. The notebook doubles as the final report with math, code, tests, and experiments.

## Environment
- Python 3.12
- Key packages: numpy 2.3.2, pandas 2.3.2, matplotlib 3.10.5, scikit-learn 1.7.1, pytest 8.4.1

```bash
python -m venv .venv
source .venv/bin/activate
pip install numpy==2.3.2 pandas==2.3.2 matplotlib==3.10.5 scikit-learn==1.7.1 pytest==8.4.1
```

## Repo Structure
- `src/project.ipynb` – report + implementation + tests + experiments
- `data/` – train/validation splits of the Breast Cancer Wisconsin dataset
- `cart_depth_analysis.png` – depth vs. accuracy plot generated in Part 4
- `LICENSE` – MIT

## How to Run
1. Open `src/project.ipynb` and run cells in order.
2. Part 2 defines the CART class (NumPy only).
3. Part 3 runs unit tests (method-by-method), sklearn parity checks, and loss verification.
4. Part 4 trains on the Breast Cancer Wisconsin data, compares against sklearn, and saves the depth sweep plot.

## Authors
- Sibo Zhou
- Shiyu Liu
- Ruoyun Yang
- Zhaocheng Yang