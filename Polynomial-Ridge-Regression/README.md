# Polynomial and Ridge Regression

This section of the **Core-ML-DS-Techniques** repository dives into **Polynomial Regression** and **Ridge Regression**, two powerful extensions of linear regression for modeling more complex relationships and addressing overfitting in data. This guide provides essential equations, detailed explanations, and practical code examples for both methods.

---

## 📖 Overview

- **Polynomial Regression**: Allows for capturing nonlinear relationships by introducing polynomial terms in the features.
- **Ridge Regression**: A regularization technique that penalizes large coefficients to control model complexity, preventing overfitting.

These methods are widely used for datasets where linear models may not suffice or when there's a need to balance model flexibility with robustness.

---

## ✏️ Essential Equations

### 1. **Polynomial Regression**

Polynomial Regression builds on linear regression by adding polynomial terms, allowing for the modeling of nonlinear relationships. For a single predictor \( x \) and polynomial degree \( d \), the model is expressed as:

\[
$y = \beta_0 + \beta_1 x + \beta_2 x^2 + \dots + \beta_d x^d + \epsilon$
\]

- \( $\beta_0, \beta_1, \dots, \beta_d$ \): Coefficients of the polynomial terms
- \( $d$ \): Degree of the polynomial
- \( $\epsilon$ \): Error term

In matrix notation, Polynomial Regression can be represented by expanding \( X \) with polynomial terms up to degree \( d \):

\[
$y = X \beta + \epsilon$
\]

where \( $X$ \) includes the powers of \( $x$ \) for each degree up to \( $d$ \).

### 2. **Ridge Regression**

Ridge Regression, also known as **L2 Regularization**, extends linear (or polynomial) regression by adding a penalty term to the loss function. This penalty controls the size of coefficients, reducing the risk of overfitting, especially in high-dimensional or collinear data.

The objective function for Ridge Regression is:

\[
\text{Minimize } \sum_{i=1}^m \left( y_i - \hat{y}_i \right)^2 + \lambda \sum_{j=1}^n \beta_j^2
\]

where:
- \( \sum_{i=1}^m (y_i - \hat{y}_i)^2 \): Sum of Squared Errors (SSE)
- \( \lambda \): Regularization parameter controlling the penalty strength
- \( \sum_{j=1}^n \beta_j^2 \): L2 norm (penalty term) on the coefficients

### 3. **Coefficient Calculation in Ridge Regression**

The Ridge Regression coefficients are calculated using the following closed-form solution in matrix notation:

\[
\beta = (X^T X + \lambda I)^{-1} X^T y
\]

where:
- \( X \): Matrix of input features, including polynomial terms for Polynomial Ridge Regression
- \( y \): Vector of output values
- \( \lambda I \): Regularization term, with \( I \) as the identity matrix

Increasing \( \lambda \) forces smaller coefficients, thus simplifying the model, while setting \( \lambda = 0 \) reverts the model to regular Polynomial Regression.

---

## 📊 Visualizing the Results

For both Polynomial and Ridge Regression, visualization is key to understanding model performance. Comparing fitted curves or surfaces with the data points helps in assessing model accuracy, especially when tuning the degree \( d \) in Polynomial Regression or the regularization parameter \( \lambda \) in Ridge Regression.

---

## 💻 Getting Started

To experiment with Polynomial and Ridge Regression, clone the repository and navigate to this section:

```bash
git clone https://github.com/leem18/Core-ML-DS-Techniques.git
cd Core-ML-DS-Techniques/Polynomial-Ridge-Regression
```

## 🤔 Why Use Polynomial and Ridge Regression?
Polynomial Regression enables modeling of complex, nonlinear relationships that simple linear models cannot capture.
Ridge Regression adds robustness, making it valuable for high-dimensional data or when multicollinearity is present.
Combined, these techniques provide a flexible yet controlled approach to regression modeling, balancing accuracy and generalizability.
