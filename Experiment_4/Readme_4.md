Objective:

WAP to evaluate the performance of implemented three-layer neural network with
variations in activation functions, size of hidden layer, learning rate.


Description of the Model:

The model consists of three layers:
Input Layer: Accepts 784-dimensional flattened images (28x28 pixels).
Hidden Layer: Experimented with different sizes (256, 128, 64 neurons) and activation functions (ReLU, Sigmoid, Tanh).
Output Layer: Contains 10 neurons corresponding to the 10 digit classes, with a softmax activation function to classify the input.
The network is trained using categorical cross-entropy loss and optimized using Adam Optimizer. The learning rate is set to 0.01, and the model is trained for 50 epochs with a batch size of 10.


Performance Evaluation:

Accuracy: The model's accuracy is evaluated for different activation functions and hidden layer sizes.
Loss Curve: The loss is tracked over 50 epochs to monitor the convergence of the model.
Confusion Matrix: Displays the classification performance across the 10 digit classes.
Execution Time: Measures the time taken for training with different configurations.
More details in the word xml file 

My Comments:

1.The model accuracy changes according to activation function and hidden layer size
2.Sigmoid activation function with 256 hidden units, achieving a test accuracy of 0.9682 (96.82%) has the most highest test accuracy.


Limitations:
1.Normal CPU works slow and hence a GPU would do this task more faster.
2.Increasig the number of hidden layer size will increase the time for execution and calculation

Future Improvements:
1. using deeper network for better performance and additional hyperparameters.