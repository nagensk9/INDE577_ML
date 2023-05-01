
# Support Vector Machines 

## Introduction
<p align="center"><img src="https://github.com/nagensk9/INDE577_ML/blob/main/1.%20Supervised%20Machine%20Learning/7-%20Support%20Vector%20Machine/images/SVM_def.png?raw=true" width=300></p><br>

Support Vector Machines (SVM) is a supervised learning algorithm that can solve linear and non-linear classification and regression problems. SVM is especially effective in scenarios where the data is not linearly separable and requires complex decision boundaries.

## How Does SVM Work?
The primary goal of SVM is to find an optimal hyperplane in a high-dimensional feature space that maximally separates the data points belonging to different classes. This hyperplane is called the **decision boundary**. SVM achieves this by transforming the input data into a higher-dimensional feature space through a **kernel function**.

<p align="center"><img src="https://github.com/nagensk9/INDE577_ML/blob/main/1.%20Supervised%20Machine%20Learning/7-%20Support%20Vector%20Machine/images/SVM.gif?raw=true" width=500></p><br>


## Introduction to Support Vector Regression (SVR)
Support Vector Regression (SVR) is a supervised learning algorithm that utilizes the principles of SVM to solve regression problems. SVR is effective when dealing with non-linear data and aims to find the best fitting hyperplane that predicts the target variable while considering a predefined tolerance for errors.

## Formulation of SVR
The goal of SVR is to find a function that predicts the target variable with the smallest possible deviation from the actual values. The formulation of SVR involves the following components:

### Decision Function
The decision function in SVR is represented as follows:

**y = w^T * x + b**

where **y** is the predicted target variable, **w** is the weight vector, **x** is the input data point, and **b** is the bias term.

### Loss Function
The loss function in SVR captures the deviation between the predicted target variable and the actual values. The most commonly used loss function in SVR is the **epsilon-insensitive loss function**, which is defined as:

**L(y, y') = max(0, |y - y'| - epsilon)**

where **y** is the actual target value, **y'** is the predicted target value, and **epsilon** is a predefined tolerance parameter that controls the acceptable deviation.

### Objective Function
The objective function in SVR combines the loss function with a regularization term to find the best fitting hyperplane. The objective function is defined as:

**minimize (1/2) * ||w||^2 + C * Σ L(y, y')**

where **||w||^2** is the L2 regularization term that penalizes complex models, **C** is the regularization parameter that balances the trade-off between the margin and the deviation, and **Σ L(y, y')** is the sum of the loss function over all data points.

### Constraints
The constraints in SVR ensure that the predicted target values fall within the tolerance region defined by the epsilon parameter. The constraints are formulated as:

**y - y' <= epsilon** (for y < y')

**y' - y <= epsilon** (for y >= y')

## Optimization in Support Vector Regression
The optimization problem in SVR involves finding the best fitting hyperplane that minimizes the objective function while satisfying the constraints. This optimization problem can be solved using techniques such as **Sequential Minimal Optimization (SMO)**, which iteratively updates the Lagrange multipliers and the support vectors until convergence is reached.

## Evaluation Metrics for Support Vector Regression
To assess the performance of an SVR model, several evaluation metrics can be used:


### Mean Squared Error (MSE)
MSE is calculated as:

*MSE = (1/n) Σ(y - y')^2*

where *y* is the actual target value, *y'* is the predicted target value, and *n* is the number of data points.

### Root Mean Squared Error (RMSE)
RMSE is calculated as:

*RMSE = sqrt(MSE)*

### Coefficient of Determination (R-squared)
R-squared is calculated as:

*R^2 = 1 - (Σ(y - y')^2 / Σ(y - y_mean)^2)*

where *y* is the actual target value, *y'* is the predicted target value, and *y_mean* is the mean of the actual target values.

R-squared ranges from 0 to 1, with a higher value indicating a better fit of the SVR model to the data.
