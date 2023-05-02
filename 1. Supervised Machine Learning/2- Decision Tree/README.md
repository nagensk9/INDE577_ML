
# Decision Trees


## Introduction
A Decision Tree is a flowchart-like structure that represents a series of decisions and their potential consequences. Each internal node of the tree represents a decision based on a specific feature, while the leaf nodes represent the outcomes or predicted values. Decision Trees are intuitive and easy to interpret, making them useful for both exploratory analysis and decision-making tasks.
<p align="center"><img src="https://annalyzin.files.wordpress.com/2016/07/decision-trees-example-multiple-categories-tutorial2.png" width=600></p>

## Construction of Decision Trees
The construction of a Decision Tree involves the following steps:

1. Selecting the best feature: At each internal node, a feature is chosen based on certain criteria such as information gain or Gini impurity. The feature with the most discriminatory power is selected to split the data.

2. Splitting the data: The selected feature is used to partition the dataset into subsets based on its possible values or thresholds. Each subset is associated with a child node in the tree.

3. Recursion: The process is recursively applied to each child node until a stopping criterion is met. This can be a predefined maximum depth, a minimum number of samples per leaf, or when further splitting does not improve the model's performance.

4. Assigning labels or values: Once the tree is constructed, the leaf nodes are assigned class labels in the case of classification or predicted values in the case of regression.

## Evaluation and Pruning
To avoid overfitting and improve the generalization ability of Decision Trees, evaluation and pruning techniques are employed. These techniques include:

- **Cross-Validation**: Cross-validation helps estimate the performance of the Decision Tree model on unseen data. It involves splitting the dataset into multiple subsets for training and testing.

- **Pruning**: Pruning involves removing unnecessary nodes from the tree to prevent overfitting. This can be achieved by setting a minimum improvement threshold or using cost-complexity pruning algorithms.

## Evaluation Metrics
The performance of Decision Trees can be assessed using various evaluation metrics, including:

- **Classification Accuracy**: Classification accuracy measures the proportion of correctly classified instances over the total number of instances.

- **Confusion Matrix**: A confusion matrix provides a detailed breakdown of the model's predictions and the true class labels, showing the counts of true positives, true negatives, false positives, and false negatives.

- **Information Gain**: Information gain measures the reduction in entropy or impurity after a split. It quantifies the amount of information gained by splitting the data based on a particular feature.

- **Gini Impurity**: Gini impurity is a measure of the probability of misclassifying an instance in a dataset. It assesses the purity of a set of instances and is used to evaluate the quality of splits in Decision Trees.
