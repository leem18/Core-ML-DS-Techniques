# K-Nearest Neighbor (KNN)

This section of the **Core-ML-DS-Techniques** repository focuses on **K-Nearest Neighbor (KNN)**, an instance-based algorithm commonly used for classification and regression tasks. KNN is a straightforward yet effective technique that leverages the concept of distance to make predictions based on the closest data points. This README provides key equations, explanations, and hands-on examples for applying KNN to real-world data.

---

## 📖 Overview

The **K-Nearest Neighbor** algorithm is based on finding a fixed number of training samples closest in distance to a new data point and making predictions based on these "neighbors." KNN is intuitive, easy to implement, and highly effective for many applications, including image and speech recognition.

---

## ✏️ Essential Equations

### 1. **Distance Metric**

KNN relies on a distance metric to identify the closest neighbors. The most commonly used distance measure is the **Euclidean Distance**. For two points $X = (x_1, x_2, \dots, x_n)$ and $Y = (y_1, y_2, \dots, y_n)$, the Euclidean distance is calculated as:

\[
$d(X, Y) = \sqrt{\sum_{i=1}^n (x_i - y_i)^2}$
\]

Alternative distance measures can also be used depending on the dataset, such as **Manhattan Distance**:

\[
$d(X, Y) = \sum_{i=1}^n |x_i - y_i|$
\]

### 2. **KNN for Classification**

In classification tasks, KNN predicts the class of a new data point by identifying the $K$ nearest points and using a majority voting system. The predicted class $\hat{y}$ is the class most frequently occurring among the $K$ neighbors:

\[
$\hat{y} = \text{mode}(y_1, y_2, \dots, y_K)$
\]

where $y_1, y_2, \dots, y_K$ represent the classes of the nearest neighbors.

### 3. **KNN for Regression**

For regression, KNN calculates the prediction $\hat{y}$ for a new data point as the **average** of the values of the $K$ nearest neighbors:

\[
$\hat{y} = \frac{1}{K} \sum_{i=1}^K y_i$
\]

where $y_i$ are the target values of the nearest neighbors. This approach provides a smooth estimation based on the local data points around the query.

---

## 📊 Choosing the Right $K$ Value

The parameter $K$ (number of neighbors) is critical to KNN performance:
- A **small $K$** makes the model sensitive to noise, potentially leading to overfitting.
- A **large $K$** smooths the decision boundary, which may lead to underfitting.

Choosing $K$ typically involves cross-validation to identify the value that minimizes prediction error.

---

## 💻 Getting Started

To experiment with K-Nearest Neighbor, clone the repository and navigate to this section:

```bash
git clone https://github.com/leem18/Core-ML-DS-Techniques.git
cd Core-ML-DS-Techniques/K-Nearest-Neighbor
```

## 🤔 Why Use K-Nearest Neighbor?
Simple and Intuitive: KNN is easy to understand and implement.
Non-parametric: KNN makes no assumptions about data distribution, making it versatile.
Effective for Diverse Applications: Commonly used in image recognition, anomaly detection, and recommendation systems.
K-Nearest Neighbor is a powerful tool for instance-based learning, offering a balance of simplicity and flexibility in both classification and regression tasks.
