# CART: Classification and Regression Tree Implementation

**GitHub Repository:** https://github.com/cynthiayry/DATA2060-Machine-Learning-Algorithm-Project--CART

A robust, from-scratch implementation of the CART (Classification and Regression Trees) algorithm for classification tasks, developed as part of the DATA2060 Machine Learning course.

This project implements the CART algorithm (Breiman et al., 1984) using only **Python** and **NumPy**, mirroring the API of `sklearn.tree.DecisionTreeClassifier`. It demonstrates a deep understanding of recursive partitioning, Gini impurity optimization, and tree-based inference.

## Key Features

*   **Scikit-learn API Compatibility**: Implements `fit`, `predict`, `predict_proba`, and `score` methods for seamless integration.
*   **Feature Importance**: Calculates Gini importance for interpretability, allowing users to identify the most predictive features.
*   **Tree Visualization**: Includes a `print_tree` method to visualize the decision logic in a human-readable format.
*   **Hyperparameter Control**: Supports `max_depth`, `min_samples_split`, and `min_samples_leaf` to manage the bias-variance trade-off.
*   **Comprehensive Testing**: Validated against scikit-learn with a rigorous suite of unit tests covering edge cases, depth constraints, and probability estimates.

## Repository Structure

```
├── data/                    # Train/validation splits of Breast Cancer Wisconsin dataset
│   ├── X_train.csv
│   ├── y_train.csv
│   ├── X_val.csv
│   └── y_val.csv
├── src/
│   ├── project.ipynb        # Main Jupyter Notebook (Report + Code + Tests)
│   └── cart_depth_analysis.png # Generated analysis plot
├── .gitignore
├── LICENSE                  # MIT License
├── README.md
├── requirements.txt         # Python package dependencies
└── Final project rubric.pdf
```

## Environment

This project was developed using:
- **Python:** 3.12.11
- **Key packages:** numpy 2.3.2, pandas 2.3.2, matplotlib 3.10.5, scikit-learn 1.7.1, pytest 8.4.1, torch 2.7.1

## Installation & Usage

### Installation

To reproduce the environment and run the code locally:

```bash
# Clone the repository
git clone https://github.com/cynthiayry/DATA2060-Machine-Learning-Algorithm-Project--CART.git
cd DATA2060-Machine-Learning-Algorithm-Project--CART

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

Alternatively, using conda:

```bash
conda create -n cart python=3.12
conda activate cart
pip install -r requirements.txt
```

### Running the Project

Open `src/project.ipynb` in Jupyter Lab or VS Code. The notebook is self-contained and structured as follows:

**Part 1 - Overview**: Mathematical formulation of CART and Gini Impurity.
**Part 2 - Model**: The core `DecisionTreeClassifier` class implementation.
**Part 3 - Check Model**: Unit tests and parity checks against `sklearn`.
**Part 4 - Main**: End-to-end experiment on Breast Cancer data, including feature importance analysis and depth tuning.

## Performance

Our implementation achieves parity with scikit-learn on the Breast Cancer Wisconsin dataset:

| Metric | Our CART | Sklearn CART |
|--------|----------|--------------|
| **Validation Accuracy** | ~93% | ~92% |
| **Tree Depth** | 5 | 5 |

*Note: Slight variations in accuracy may occur due to floating-point precision differences in split threshold selection.*

## Authors

- **Ruoyun Yang** - Brown University - ruoyun_yang@brown.edu
- **Shiyu Liu** - Brown University - shiyu_liu1@brown.edu
- **Zhaocheng Yang** - Brown University - zhaocheng_yang@brown.edu
- **Sibo Zhou** - Brown University - sibo_zhou@brown.edu

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## References

*   Breiman, L., Friedman, J., Olshen, R., & Stone, C. (1984). *Classification and Regression Trees*. Wadsworth.
*   Pedregosa, F. et al. (2011). Scikit-learn: Machine learning in Python. *JMLR*.
