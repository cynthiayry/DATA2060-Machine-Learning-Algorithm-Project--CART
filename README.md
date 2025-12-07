# CART: Classification and Regression Tree Implementation

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
├── data/                  # Dataset files (Breast Cancer Wisconsin)
│   ├── X_train.csv
│   ├── y_train.csv
│   └── ...
├── src/
│   ├── project.ipynb      # Main Jupyter Notebook (Report + Code + Tests)
│   └── cart_depth_analysis.png # Generated analysis plot
├── README.md              # Project documentation
├── LICENSE                # MIT License
└── Final project rubric.md
```

## Installation & Usage

The project requires Python 3.12+. We recommend using a virtual environment.

```bash
# Clone the repository
git clone https://github.com/yourusername/cart-project.git
cd cart-project

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install numpy pandas matplotlib scikit-learn pytest
```

### Running the Project

Open `src/project.ipynb` in Jupyter Lab or VS Code. The notebook is self-contained and structured as follows:

1.  **Overview**: Mathematical formulation of CART and Gini Impurity.
2.  **Model**: The core `DecisionTreeClassifier` class implementation.
3.  **Check Model**: Unit tests and parity checks against `sklearn`.
4.  **Main**: End-to-end experiment on Breast Cancer data, including feature importance analysis and depth tuning.

## Performance

Our implementation achieves parity with scikit-learn on the Breast Cancer Wisconsin dataset:

| Metric | Our CART | Sklearn CART |
|--------|----------|--------------|
| **Validation Accuracy** | ~93% | ~92% |
| **Tree Depth** | 5 | 5 |

*Note: Slight variations in accuracy may occur due to floating-point precision differences in split threshold selection.*

## Contributors

*   **Sibo Zhou**
*   **Shiyu Liu**
*   **Ruoyun Yang**
*   **Zhaocheng Yang**

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## References

*   Breiman, L., Friedman, J., Olshen, R., & Stone, C. (1984). *Classification and Regression Trees*. Wadsworth.
*   Pedregosa, F. et al. (2011). Scikit-learn: Machine learning in Python. *JMLR*.
