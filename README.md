# Machine Learning from Scratch

A structured collection of machine learning algorithm implementations written in Python, built from the ground up without relying on high-level library wrappers. Each topic includes a from-scratch implementation, a parallel scikit-learn comparison, and one or more project notebooks applied to toy or real-world datasets.

Built every algorithm by hand. Verified against scikit-learn. No black boxes.

---

## Repository Structure

### Algorithm Implementations

| Folder | Category | Description |
|---|---|---|
| `Linear_Regression/` | Supervised | Simple and multiple linear regression, assumptions, gradient descent |
| `Logistic Regression/` | Supervised | Perceptron trick, sigmoid, gradient descent for classification |
| `DecisionTrees/` | Supervised | Geometric intuition, regression trees, housing price prediction |
| `KNN/` | Supervised | From-scratch KNN, breast cancer prediction project |
| `SVM/` | Supervised | Hard-margin SVM, kernel SVM |
| `Random_Forest/` | Ensemble | Intro, bagging vs random forest comparison, hyperparameter tuning |
| `Bagging/` | Ensemble | Bagging implementation and classifier experiments |
| `Regularization/` | Optimization | Ridge regression, Lasso regression, sparsity |
| `Markov-Chain/` | Probabilistic | Bigram text generator using Markov transition matrix |

### Practice & Data Engineering

These folders don't contain algorithm implementations — they cover data preprocessing, exploratory analysis, and pipeline tooling practiced alongside the core ML work.

| Folder | Category | Description |
|---|---|---|
| `EDA/` | Data Analysis | Univariate and bivariate analysis |
| `Feature_engineering/` | Preprocessing | Encoding, scaling, column transformers |
| `Outliers/` | Preprocessing | Outlier detection and handling |
| `ML_Pipelines/` | Engineering | Sklearn pipelines applied to Titanic dataset |
| `Pandas Profiling/` | Data Analysis | Automated EDA reports using pandas profiling |

---


## Projects

### Mini Projects

Most algorithm folders include at least one applied notebook on a real or toy dataset:

| Project | Folder | Notebook / File |
|---|---|---|
| Breast cancer classification | `KNN/` | `01_BreastCancerPredictionModel.ipynb` |
| Housing price prediction (regression trees) | `DecisionTrees/` | `02_RegressionTreesFromSCRATCH.ipynb` + `HousingData.csv` |
| Titanic survival prediction (full pipeline) | `ML_Pipelines/` | `titanic.ipynb` |
| Heart disease classification | `Random_Forest/` | `01_intro.ipynb` + `heart.csv` |
| Placement outcome analysis | `Outliers/` | `project.ipynb` |

---

## End-to-End: Credit Card Fraud Detection

A full production-grade project built on the [ULB Credit Card Fraud dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). Covers full preprocessing, model development (Random Forest & XGBoost), hyperparameter tuning, and a production-ready FastAPI backend — containerized with Docker and deployed on Render.

| Resource | Link |
|---|---|
| GitHub Repo | [moksh-m9u/Credit-Card-Fraud-Detection](https://github.com/moksh-m9u/Credit-Card-Fraud-Detection) |
| Docker Image | [mokshm9u/project-server](https://hub.docker.com/r/mokshm9u/project-server) |
| Live API (Swagger) | [credict-card-server.onrender.com/docs](https://credict-card-server.onrender.com/docs) |
| Kaggle Dataset | [mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) |

---



## Folder Breakdown

### Linear Regression

Four notebooks covering:
- Simple linear regression with visualization
- From-scratch implementation
- Multiple linear regression
- Assumptions of linear regression (linearity, homoscedasticity, normality of residuals)

**Gradient Descent** (`Linear_Regression/GradientDescent/`) — Five progressive notebooks:
1. Step-by-step gradient descent mechanics
2. General gradient descent
3. End-to-end GD applied to linear regression
4. Batch gradient descent for N features
5. Stochastic gradient descent (SGD)

Datasets used: placement data, salary data, general regression data.

### Logistic Regression

- Perceptron trick implementation
- Sigmoid function derivation
- Gradient descent for logistic regression
- Full end-to-end classification notebook with `placement.csv`

### Decision Trees

- Geometric intuition and splitting criteria
- Decision tree regressors applied to housing data

### K-Nearest Neighbors

- Breast cancer prediction project using the full Kaggle dataset
- From-scratch KNN implementation validated against sklearn

### Support Vector Machines

- Hard-margin SVM derivation and implementation
- Kernel SVM notebook (RBF and polynomial kernels)

### Regularization

**Ridge (L2)**
- Introduction and properties
- Applied to multiple linear regression
- Ridge via gradient descent
- Key understandings notebook

**Lasso (L1)**
- Introduction
- Properties of Lasso vs Ridge
- Understanding sparsity in Lasso

### Bagging and Random Forest

- Bagging from scratch and classifier experiments
- Intro to Random Forest
- Bagging vs Random Forest comparison
- Hyperparameter tuning with GridSearchCV

### Markov Chain

- Bigram-based text generation
- Builds a transition probability matrix from input text
- Generates new sequences by sampling from learned probabilities

### EDA

- Univariate analysis: distributions, histograms, box plots
- Bivariate analysis: correlations, scatter plots, cross-tabs using Iris, Titanic, and Tips datasets

### Feature Engineering

- **Encoding**: Ordinal encoding, nominal/one-hot encoding
- **Scaling**: Normalization, standardization
- **Column Transformer**: Combining multiple preprocessing steps

### ML Pipelines

- Full Titanic pipeline with preprocessing and a classifier
- Comparison notebook showing the same workflow without a pipeline
- Exported `pipe.pkl` for deployment reference

### Outliers

- Detection and treatment methods
- Applied to a placement dataset project

### Pandas Profiling

- Automated profiling reports for Titanic dataset
- Exported HTML reports for offline review

---

## Prerequisites

```
python >= 3.9
numpy
pandas
scikit-learn
matplotlib
seaborn
jupyter
nltk             # for Markov-Chain
ydata-profiling  # for Pandas Profiling
```

Install all dependencies:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter nltk ydata-profiling
```

---

## Running the Code

**Jupyter notebooks:**
```bash
jupyter notebook
```

---

## License

This repository is open source. You are free to use, fork, and adapt any implementation for your own learning or projects.
