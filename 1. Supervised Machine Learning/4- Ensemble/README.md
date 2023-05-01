
# Ensemble Learning (XGBoost)


## Overview
<p align="center"><img src="https://github.com/nagensk9/INDE577_ML/blob/main/1.%20Supervised%20Machine%20Learning/4-%20Ensemble/images/Ensemble_.png?raw=true" width=600 height=400></p><br>
- Ensemble learning is a powerful approach in machine learning that combines the predictions of multiple models to make accurate and robust predictions.
- Boosting and Bagging are two popular techniques used in ensemble learning.
- This comprehensive guide will introduce you to ensemble learning, specifically focusing on Boosting and Bagging, and provide implementations in Python using real-world datasets.

## Introduction to Ensemble Learning
Ensemble learning is a technique where multiple models are combined to make predictions. The idea behind ensemble learning is that the collective knowledge of multiple models can outperform a single model. By leveraging the strengths of different models, ensemble learning can improve prediction accuracy and reduce the risk of overfitting.

## Boosting: An Ensemble Learning Technique
Boosting is a sequential ensemble learning technique where weak learners are combined to create a strong learner. It works by iteratively training weak models, such as decision trees, and giving more importance to the misclassified instances in subsequent iterations. The final prediction is made by aggregating the predictions of all the weak models.

Boosting algorithms, such as AdaBoost and Gradient Boosting, have gained popularity due to their ability to handle complex patterns and achieve high accuracy. These algorithms aim to reduce bias and improve generalization by emphasizing the challenging instances in the training data.
<p align="center"><img src="https://github.com/nagensk9/INDE577_ML/blob/main/1.%20Supervised%20Machine%20Learning/4-%20Ensemble/images/Bagging.gif?raw=true" width=600 height=400></p><br>
## Bagging: Another Ensemble Learning Technique
Bagging, short for Bootstrap Aggregating, is another ensemble learning technique that involves training multiple models on different subsets of the training data. Each model is trained independently, and the final prediction is made by averaging or majority voting over the predictions of all the models.

Bagging algorithms, such as Random Forest, create an ensemble of decision trees. The key idea is to reduce the variance by averaging the predictions of multiple trees trained on different subsets of the data. Bagging techniques are known for their ability to handle noisy data and reduce overfitting.
<p align="center"><img src="https://github.com/nagensk9/INDE577_ML/blob/main/1.%20Supervised%20Machine%20Learning/4-%20Ensemble/images/Boosting.gif?raw=true" width=600 height=400></p><br>

## Why Do We Need Ensemble Learning?
Ensemble learning offers several advantages:

1. **Improved Accuracy**: By combining multiple models, ensemble learning can capture different aspects of the data, leading to improved accuracy compared to a single model.

2. **Robustness**: Ensemble learning can reduce the impact of outliers or noisy data points. Even if individual models make incorrect predictions, the ensemble can still provide robust predictions.

3. **Handling Complexity**: Ensemble learning can handle complex relationships between features and the target variable. The combination of multiple models with different strengths can capture intricate patterns in the data.

4. **Reducing Overfitting**: Ensemble learning techniques, such as Bagging, help reduce overfitting by training models on different subsets of the data. This diversity in training helps to create a more generalizable model.


## What is XGBoost?
XGBoost is a supervised learning algorithm that excels in regression tasks. It uses a combination of boosting and regularization techniques to improve performance and prevent overfitting. XGBoost is capable of handling both continuous and categorical variables and can handle missing data.


## XGBoost Process
The XGBoost algorithm involves the following key steps:

1. **Data Preparation**: Preprocess the dataset by handling missing values, encoding categorical variables, and scaling the features if necessary. Split the dataset into training and testing sets.

2. **Boosting Rounds**: XGBoost performs gradient boosting in multiple rounds. In each round, a decision tree is added to the ensemble, and the weights of the previous trees are adjusted.

3. **Loss Function and Optimization**: XGBoost uses a loss function to measure the difference between the predicted and actual values. It optimizes the loss function by iteratively adjusting the weights of the decision trees.

4. **Prediction**: For a new input, XGBoost combines the predictions of all the decision trees in the ensemble to obtain the final prediction. The predictions are weighted based on the importance of each tree.

## Evaluation Metrics for XGBoost
XGBoost models can be evaluated using various metrics to assess their performance. Some commonly used evaluation metrics for regression tasks include:

1. **Mean Squared Error (MSE)**: MSE measures the average squared difference between the predicted and actual values. It provides a measure of how well the model's predictions align with the true values.

2. **Root Mean Squared Error (RMSE)**: RMSE is the square root of the MSE. It represents the average deviation of the predicted values from the actual values, providing a more interpretable metric.

3. **Mean Absolute Error (MAE)**: MAE measures the average absolute difference between the predicted and actual values. It provides a measure of the average magnitude of the errors made by the model.

## Conclusion
XGBoost is a powerful ensemble learning algorithm for regression tasks, offering enhanced performance, flexibility, and feature importance analysis. 

## References
The images are taken from [here](https://machinelearningknowledge.ai/gentle-introduction-to-ensemble-learning-for-beginners)
