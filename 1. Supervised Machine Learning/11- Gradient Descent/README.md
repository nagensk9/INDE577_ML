
# Gradient Descent

## Introduction 
Gradient Descent is an iterative optimization algorithm used to find the minimum of a function. In machine learning, it is commonly employed to minimize the cost or loss function of a model by updating the parameters in the direction of steepest descent. By iteratively adjusting the parameters, Gradient Descent converges to the optimal values that result in the lowest possible cost.

## The Gradient Descent Algorithm
The Gradient Descent algorithm can be summarized in the following steps:

1. Initialize the parameters of the model with arbitrary values.
2. Compute the gradient of the cost function with respect to each parameter.
3. Update the parameters by taking a step in the direction opposite to the gradient.
4. Repeat steps 2 and 3 until convergence or a maximum number of iterations.

The key concept behind Gradient Descent is to update the parameters in proportion to the negative gradient, as this direction leads to a decrease in the cost function.

## Variants of Gradient Descent
Gradient Descent comes in various variants that differ in the way they update the parameters. Some commonly used variants include:

- **Batch Gradient Descent**: In this variant, the gradient is computed using the entire training dataset, and the parameters are updated once per epoch. It ensures convergence to the global minimum but can be computationally expensive for large datasets.

- **Stochastic Gradient Descent (SGD)**: SGD updates the parameters after processing each training instance, using a randomly sampled subset of the data. It is computationally efficient but exhibits high variance in parameter updates.

- **Mini-Batch Gradient Descent**: Mini-Batch Gradient Descent strikes a balance between Batch Gradient Descent and SGD by updating the parameters using a mini-batch of randomly sampled instances. It provides a good compromise between computational efficiency and convergence speed.

## Convergence Criteria
To determine when the Gradient Descent algorithm has converged, convergence criteria are defined. Some common criteria include:

- **Maximum number of iterations**: The algorithm stops after a predefined maximum number of iterations, even if convergence has not been reached.

- **Threshold on the change in the cost function**: The algorithm terminates when the change in the cost function between consecutive iterations falls below a specified threshold.

- **Threshold on the norm of the gradient**: The algorithm stops when the norm of the gradient (the magnitude of the gradient vector) becomes smaller than a predefined threshold.

## The Mathematics of Gradient Descent
To understand the mathematics behind Gradient Descent, let's consider a cost function *J* that depends on the parameters *θ* of the model. The goal is to find the values of *θ* that minimize *J*.

The update rule for parameter *θ_j* in Gradient Descent is given by:

![Gradient Descent Update Rule](https://latex.codecogs.com/png.latex?%5Ctheta_j%20%5Cleftarrow%20%5Ctheta_j%20-%20%5Calpha%20%5Cfrac%7B%5Cpartial%20J%7D%7B%5Cpartial%20%5Ctheta_j%7D)

where *α* is the learning rate, determining the rate at which the parameters are updated. The partial derivative term, ![Partial Derivative Term](https://latex.codecogs.com/png.latex?%5Cfrac%7B%5Cpartial%20J%7D%7B%5Cpartial%20%5Ctheta_j%7D), represents the rate of change of the cost function with respect to the parameter *θ_j*.

For a linear regression model with mean squared error (MSE) as the cost function, the update rule for the parameter *θ_j* can be derived as follows:

![Gradient Descent Update Rule for Linear Regression](https://latex.codecogs.com/png.latex?%5Ctheta_j%20%5Cleftarrow%20%5Ctheta_j%20-%20%5Calpha%20%5Cfrac%7B1%7D%7Bm%7D%20%5Csum_%7Bi%3D1%7D%5E%7Bm%7D%20%28h_%5Ctheta%28x%5E%7B%28i%29%7D%29%20-%20y%5E%7B%28i%29%7D%29%20x_j%5E%7B%28i%29%7D)

where *m* is the number of training instances, *h_θ(x^(i))* is the predicted value for the *i*-th instance, *y^(i)* is the true label for the *i*-th instance, and *x_j^(i)* is the *j*-th feature value of the *i*-th instance.

The update rule involves computing the difference between the predicted and true values, multiplied by the corresponding feature value, and scaled by the learning rate. This process is repeated for each parameter *θ_j*.