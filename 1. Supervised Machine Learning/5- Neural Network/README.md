
# Neural Networks: 

## Overview
Neural Networks are powerful machine learning models inspired by the structure and functioning of the human brain. They are widely used for various tasks, including classification, regression, image recognition, and natural language processing. This comprehensive guide will provide an in-depth understanding of Neural Networks, including their architecture, activation functions, training algorithms, regularization techniques, and implementation in Python.

## Introduction
Neural Networks are a class of machine learning models that consist of interconnected artificial neurons, also known as nodes or units. These nodes are organized into layers, including an input layer, one or more hidden layers, and an output layer. Neural Networks are capable of learning complex patterns and relationships from data by adjusting the weights and biases associated with the connections between the nodes.
<p align="center"><img src="https://miro.medium.com/v2/resize:fit:1400/1*bhFifratH9DjKqMBTeQG5A.gif" width=700></p>


## Neural Network Architecture
The architecture of a Neural Network is defined by the number of layers, the number of nodes in each layer, and the connectivity pattern between the nodes. The most common architecture is the Feedforward Neural Network, where the information flows from the input layer to the output layer without cycles. However, there are other types of Neural Networks, such as Recurrent Neural Networks (RNNs) and Convolutional Neural Networks (CNNs), designed for specific tasks.

## Activation Functions
Activation functions introduce non-linearity into the Neural Network, enabling it to learn complex relationships. Commonly used activation functions include:

- **Sigmoid Function**: The sigmoid function maps the input to a value between 0 and 1, providing smooth and bounded outputs. It is given by the formula: 

   ![Sigmoid Function](https://latex.codecogs.com/png.latex?%5Csigma%28x%29%20%3D%20%5Cfrac%7B1%7D%7B1%20&plus;%20e%5E%7B-x%7D%7D)

- **ReLU (Rectified Linear Unit)**: ReLU is a piecewise linear function that outputs the input if it is positive and 0 otherwise. It is defined as:

   ![ReLU Function](https://latex.codecogs.com/png.latex?%5Ctext%7BReLU%7D%28x%29%20%3D%20%5Cmax%280%2C%20x%29)

- **Hyperbolic Tangent (Tanh)**: Tanh is similar to the sigmoid function but maps the input to a value between -1 and 1. It is given by:

   ![Tanh Function](https://latex.codecogs.com/png.latex?%5Ctanh%28x%29%20%3D%20%5Cfrac%7Be%5E%7Bx%7D%20-%20e%5E%7B-x%7D%7D%7Be%5E%7Bx%7D%20&plus;%20e%5E%7B-x%7D%7D)

**Softmax Function**: Softmax is used in the output layer of Neural Networks for multi-class classification. It converts the inputs into a probability distribution over the classes. The softmax function is given by:

   ![Softmax Function](https://latex.codecogs.com/png.latex?%5Ctext%7Bsoftmax%7D%28x_i%29%20%3D%20%5Cfrac%7Be%5E%7Bx_i%7D%7D%7B%5Csum_%7Bj%3D1%7D%5E%7Bn%7De%5E%7Bx_j%7D%7D)

where *x_i* represents the input value for class *i*, and *n* is the total number of classes.

## Training Neural Networks
Training Neural Networks involves adjusting the weights and biases to minimize the difference between the predicted outputs and the true targets. This process is accomplished through the following steps:

Sure! Here are some of the basic formulas for a Neural Network:

1. **Weighted Sum Calculation**: The weighted sum of inputs for a neuron *j* in layer *l* is calculated as:

   ![Weighted Sum Calculation](https://latex.codecogs.com/png.latex?z_j%5El%20%3D%20%5Csum_%7Bi%7D%20w_%7Bij%7D%5El%20a_i%5E%7Bl-1%7D%20&plus;%20b_j%5El)

   where *w_ij^l* represents the weight between neuron *i* in layer *l-1* and neuron *j* in layer *l*, *a_i^(l-1)* is the activation of neuron *i* in layer *l-1*, and *b_j^l* is the bias term for neuron *j* in layer *l*.

2. **Activation Calculation**: The activation of a neuron *j* in layer *l* is obtained by applying an activation function, denoted as *σ*, to the weighted sum:

   ![Activation Calculation](https://latex.codecogs.com/png.latex?a_j%5El%20%3D%20%5Csigma%28z_j%5El%29)

   where *a_j^l* represents the activation of neuron *j* in layer *l*.

3. **Output Calculation**: The output of the Neural Network is obtained from the activations of the neurons in the output layer. The specific formula depends on the task (classification, regression, etc.) and the activation function used in the output layer.

4. **Loss Function**: The loss function measures the discrepancy between the predicted outputs and the true targets. The choice of the loss function depends on the task (e.g., Mean Squared Error for regression, Cross-Entropy Loss for classification).

	  **Mean Squared Error (MSE)**: MSE is a commonly used loss function for regression tasks. It calculates the average squared difference between the predicted outputs (_y_hat_) and the true target values (_y_) over a dataset of _n_ samples:
    
    ![MSE](https://latex.codecogs.com/png.latex?%5Ctext%7BMSE%7D%20%3D%20%5Cfrac%7B1%7D%7Bn%7D%20%5Csum_%7Bi%3D1%7D%5En%20%28y_i%20-%20%5Chat%7By_i%7D%29%5E2)
    
	 **Cross-Entropy Loss**: Cross-entropy loss is commonly used for classification tasks. It measures the dissimilarity between the predicted class probabilities (_y_hat_) and the true class labels (_y_):
    
    ![Cross-Entropy Loss](https://latex.codecogs.com/png.latex?%5Ctext%7BCross-Entropy%20Loss%7D%20%3D%20-%5Csum_%7Bi%3D1%7D%5En%20%28y_i%20%5Clog%28%5Chat%7By_i%7D%29%29)

5. **Backpropagation**: Backpropagation is a technique used to compute the gradients of the loss function with respect to the weights and biases. It involves propagating the error backward through the network, updating the weights and biases based on the computed gradients.<br>
	![Gradient Calculation for Weights](https://latex.codecogs.com/png.latex?%5Cfrac%7B%5Cpartial%20%7B%5Ctext%7BLoss%7D%7D%7D%7B%5Cpartial%20w_%7Bij%7D%5El%7D%20%3D%20%5Cfrac%7B%5Cpartial%20%7B%5Ctext%7BLoss%7D%7D%7D%7B%5Cpartial%20z_j%5El%7D%20%5Ccdot%20%5Cfrac%7B%5Cpartial%20z_j%5El%7D%7B%5Cpartial%20w_%7Bij%7D%5El%7D)

	where _∂Loss/∂z_j^l_ represents the partial derivative of the loss with respect to the weighted sum of neuron _j_ in layer _l_, and _∂z_j^l/∂w_ij^l_ is the partial derivative of the weighted sum with respect to the weight _w_ij^l_.

7. **Gradient Descent**: Gradient Descent is an optimization algorithm used to update the weights and biases based on the computed gradients. It involves multiplying the gradients by a learning rate and subtracting them from the current weights and biases.

8. **Epochs and Batch Size**: Training a Neural Network involves iterating over the entire dataset multiple times, where each iteration is called an epoch. In large datasets, it is common to divide the data into smaller batches for efficient computation. The batch size determines the number of samples processed before updating the weights.

## Regularization Techniques
Regularization techniques are used to prevent overfitting and improve the generalization ability of Neural Networks. Some commonly used regularization techniques include:

- **L1 and L2 Regularization**: L1 and L2 regularization add a penalty term to the loss function that discourages large weights. L1 regularization promotes sparsity in the weights, while L2 regularization encourages small weights. The regularization term is controlled by a hyperparameter called the regularization parameter (lambda).

- **Dropout**: Dropout randomly sets a fraction of the node activations to zero during training, which helps prevent over-reliance on specific nodes and encourages the network to learn more robust representations.

- **Early Stopping**: Early stopping involves monitoring the validation loss during training and stopping the training process when the validation loss starts to increase. This helps prevent overfitting by finding the optimal point of training where the model performs best on unseen data.

## Conclusion
Neural Networks are versatile models that have revolutionized the field of machine learning. With their ability to learn complex patterns and relationships from data, they have achieved remarkable success in various domains.
