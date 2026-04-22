# Machine Learning from Scratch

A structured collection of machine learning algorithm implementations written in Python, built from the ground up without relying on high-level library wrappers. Each topic includes a from-scratch implementation, a parallel scikit-learn comparison, and one or more project notebooks applied to toy or real-world datasets.

Built every algorithm by hand. Verified against scikit-learn. No black boxes.

---

## Repository Structure

| Folder | Category | Description |
|---|---|---|
| `Linear_Regression/` | Supervised | Simple and multiple linear regression, assumptions |
| `Logistic Regression/` | Supervised | Perceptron trick, sigmoid, gradient descent for classification |
| `DecisionTrees/` | Supervised | Geometric intuition, regression trees, housing price prediction |
| `KNN/` | Supervised | From-scratch KNN, breast cancer prediction project |
| `SVM/` | Supervised | Hard-margin SVM, kernel SVM |
| `Random_Forest/` | Ensemble | Intro, bagging vs random forest comparison, hyperparameter tuning |
| `Bagging/` | Ensemble | Bagging implementation and classifier experiments |
| `GradientDescent/` | Optimization | Step-by-step GD, batch GD, SGD, multi-feature GD |
| `Regularization/` | Optimization | Ridge regression, Lasso regression, sparsity |
| `kmeans/` | Unsupervised | K-Means from scratch, Streamlit app demo |
| `Markov-Chain/` | Probabilistic | Bigram text generator using Markov transition matrix |
| `EDA/` | Data Analysis | Univariate and bivariate analysis |
| `Feature_engineering/` | Preprocessing | Encoding, scaling, column transformers |
| `Outliers/` | Preprocessing | Outlier detection and handling project |
| `ML_Pipelines/` | Engineering | Sklearn pipelines applied to Titanic dataset |
| `Pandas Profiling/` | Data Analysis | Automated EDA reports using pandas profiling |

---

## What This Repository Contains

### Algorithm Implementations

Each supervised and unsupervised learning algorithm is implemented twice:

- **From scratch in Python** using NumPy and standard libraries, with the math made explicit in the code and notebooks.
- **Using scikit-learn** run in parallel to validate correctness and compare output.

This dual approach helps develop a clear understanding of what the library abstractions are actually doing.

### Projects

Most algorithm folders include at least one project notebook applied to a real or toy dataset. Examples include:

- Breast cancer classification using KNN (`KNN/01_BreastCancerPredictionModel.ipynb`)
- Housing price prediction using Decision Trees (`DecisionTrees/` with `HousingData.csv`)
- Titanic survival prediction using ML Pipelines (`ML_Pipelines/titanic.ipynb`)
- Heart disease classification in Random Forest (`Random_Forest/` with `heart.csv`)
- Placement outcome analysis in Outliers (`Outliers/project.ipynb`)

### Extras

- `kmeans/app.py` - A minimal Streamlit application that runs the from-scratch K-Means implementation interactively.
- `Markov-Chain/Markov_NLP.ipynb` - A bigram-based Markov chain text generator built without any ML framework.
- `ML_Pipelines/` - Demonstrates how to use `sklearn.pipeline.Pipeline` to build production-ready preprocessing and model chains, compared against a version without pipelines.

---

## Folder Breakdown

### Linear Regression

Four notebooks covering:
- Simple linear regression with visualization
- From-scratch implementation
- Multiple linear regression
- Assumptions of linear regression (linearity, homoscedasticity, normality of residuals)

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

### Gradient Descent

Five progressive notebooks:
1. Step-by-step gradient descent mechanics
2. General gradient descent
3. End-to-end GD applied to linear regression
4. Batch gradient descent for N features
5. Stochastic gradient descent (SGD)

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

### K-Means Clustering

- Full from-scratch implementation in `Kmeans.py`
- Notebook with step-by-step walkthrough
- `app.py` - interactive Streamlit demo

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
streamlit        # for kmeans/app.py
nltk             # for Markov-Chain
ydata-profiling  # for Pandas Profiling
```

Install all dependencies:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter streamlit nltk ydata-profiling
```

---

## Running the Code

**Jupyter notebooks:**
```bash
jupyter notebook
```

**K-Means Streamlit app:**
```bash
cd kmeans
streamlit run app.py
```
---
## What's Coming
Every algorithm in this repository is getting an end-to-end deployed project — a real-world dataset, full preprocessing pipeline, trained model exported as pipe.pkl, and a live Streamlit app. The idea is simple: understanding an algorithm is one thing, shipping it is another. Each project will be deployed on Streamlit Cloud so you can interact with it directly in the browser, no setup needed.

---

## License

This repository is open source. You are free to use, fork, and adapt any implementation for your own learning or projects.
