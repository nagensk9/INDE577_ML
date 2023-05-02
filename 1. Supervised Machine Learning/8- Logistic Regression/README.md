
# Logistic Regression

## Introduction
Logistic Regression is a supervised learning algorithm used for binary classification, where the target variable takes only two possible outcomes (e.g., True/False, Yes/No). It is based on the logistic function, also known as the sigmoid function, which maps any real-valued input to a value between 0 and 1. Logistic Regression models the relationship between the independent variables (features) and the probability of the target variable belonging to a certain class.
<p align="center"><img src="https://www.saedsayad.com/images/LogReg_1.png" ></p>

## Model Representation
The Logistic Regression model can be represented by the following equation:

![Logistic Regression Equation](https://latex.codecogs.com/png.latex?P%28y%20%3D%201%20%7C%20%5Cmathbf%7BX%7D%29%20%3D%20%5Cfrac%7B1%7D%7B1%20&plus;%20e%5E%7B-%28%5Cbeta_0%20&plus;%20%5Cbeta_1%20x_1%20&plus;%20%5Cbeta_2%20x_2%20&plus;%20...%20&plus;%20%5Cbeta_p%20x_p%29%7D%7D)

where:
- *P(y = 1 | X)* is the probability of the target variable *y* being 1 given the input features *X*.
- *β_0, β_1, β_2, ..., β_p* are the coefficients (parameters) of the model.
- *x_1, x_2, ..., x_p* are the values of the input features.
- *e* is the base of the natural logarithm.

The logistic function in the denominator ensures that the output probability is bounded between 0 and 1, enabling it to be interpreted as the probability of belonging to class 1.

## Training Logistic Regression
The goal of training Logistic Regression is to estimate the optimal values of the coefficients (*β*) that maximize the likelihood of the observed data. This is typically done using optimization algorithms such as Maximum Likelihood Estimation (MLE) or Gradient Descent.

During the training process, the model iteratively adjusts the coefficients based on the difference between the predicted probabilities and the actual class labels. The objective is to minimize a cost function, such as the log loss or cross-entropy loss, which quantifies the discrepancy between the predicted probabilities and the true class labels.

## Evaluation Metrics
Logistic Regression models are evaluated using various metrics to assess their performance. Some commonly used evaluation metrics include:

- **Accuracy**: Accuracy measures the proportion of correctly classified instances over the total number of instances. It is a simple and intuitive metric but may not be suitable for imbalanced datasets.

- **Precision**: Precision calculates the ratio of true positives to the sum of true positives and false positives. It quantifies the model's ability to correctly identify positive instances.

- **Recall (Sensitivity or True Positive Rate)**: Recall measures the ratio of true positives to the sum of true positives and false negatives. It quantifies the model's ability to correctly identify all positive instances.

- **F1 Score**: The F1 score is the harmonic mean of precision and recall.
- (continued)

- **Confusion Matrix**: A confusion matrix provides a detailed breakdown of the model's predictions and the true class labels, showing the counts of true positives, true negatives, false positives, and false negatives.

- **Receiver Operating Characteristic (ROC) Curve**: The ROC curve is a graphical representation of the trade-off between the true positive rate and the false positive rate. It helps assess the model's performance across different probability thresholds.

- **Area Under the ROC Curve (AUC-ROC)**: AUC-ROC summarizes the performance of the model across all possible probability thresholds. It provides a single metric that represents the overall discriminative power of the model.

## Conclusion
Logistic Regression is a powerful and widely used algorithm for binary classification tasks. It leverages the sigmoid function to model the relationship between input features and the probability of the target variable belonging to a certain class. By estimating the optimal coefficients through training, Logistic Regression can make accurate predictions and provide insights into the importance of different features.
