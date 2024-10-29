# Linear Regression

This section of the **Core-ML-DS-Techniques** repository explores **Linear Regression**, a fundamental technique in machine learning and statistics for modeling the relationship between a dependent variable and one or more independent variables. This guide provides a comprehensive overview, essential equations, and hands-on code examples to understand the workings of Linear Regression.

---

## 📖 Overview

Linear Regression is a supervised learning algorithm used for predicting a continuous target variable based on linear relationships between variables. This method is widely used in predictive modeling due to its simplicity and interpretability.

---

## ✏️ Essential Equations

### 1. **Simple Linear Regression**

In simple linear regression, we model the relationship between a single predictor variable \( x \) and a response variable \( y \) using the equation:

\[
$y = \beta_0 + \beta_1 x + \epsilon$
\]

- \( $\beta_0$ \): Intercept term, representing the value of \( $y$ \) when \( $x = 0$ \)
- \( $\beta_1$ \): Slope coefficient, representing the change in \( $y$ \) with respect to \( $x$ \)
- \( $\epsilon$ \): Error term, accounting for variance not explained by the model

### 2. **Ordinary Least Squares (OLS) Estimation**

Linear regression typically uses **Ordinary Least Squares (OLS)** to estimate the coefficients \( \beta \) by minimizing the **Sum of Squared Errors (SSE)**:

\[
$\text{SSE} = \sum_{i=1}^m (y_i - \hat{y}_i)^2 = \sum_{i=1}^m \left( y_i - \left( \beta_0 + \sum_{j=1}^n \beta_j x_{ij} \right) \right)^2$
\]

Minimizing SSE results in the best-fit line, where the predicted values are as close as possible to the observed values.

### 3. **Coefficient Calculation**

The closed-form solution for the coefficients in matrix notation is:

\[
$\beta = (X^T X)^{-1} X^T y$
\]

where:
- \( $X$ \): Matrix of input features
- \( $y$ \): Vector of output values

---

## 📊 Visualizing the Fit

In linear regression, plotting the line of best fit against the data can help visualize the model's accuracy. Residual plots, error histograms, and other visual tools are often used to assess model assumptions.

---

## 💻 Getting Started

To explore Linear Regression in action, clone the repository and open the Jupyter notebook for this section:

```bash
git clone https://github.com/leem18/Core-ML-DS-Techniques.git
cd Core-ML-DS-Techniques/Linear-Regression
```

## 🤔 Why Linear Regression?
Linear Regression offers a straightforward yet powerful method for predictive modeling. It forms the basis of more complex algorithms and is particularly useful for interpretability, allowing for clear insights into feature impact on predictions.
