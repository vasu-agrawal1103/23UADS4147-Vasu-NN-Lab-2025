Objective:
To train and evaluate a convolutional neural network (CNN) using Keras to classify the Fashion MNIST dataset and demonstrate the effects of filter size, regularization, batch size, and optimization algorithm on model performance.

Description of the Model:
The CNN consists of the following layers:
Convolutional Layers: Two convolutional layers with configurable filter sizes (3x3 or 5x5) and ReLU activation.
Pooling Layers: Max pooling layers (2x2) to downsample feature maps.
Fully Connected Layer: A dense layer with 128 neurons and ReLU activation.
Output Layer: A softmax layer with 10 neurons (corresponding to 10 Fashion MNIST classes) for classification.
Hyperparameters varied in experiments:
Filter Size: 3x3 or 5x5
Regularization: L2 regularization (0.0001 or 0.001)
Batch Size: 32 or 64
Optimization Algorithm: Adam or SGD

Python Implementation:
in exp5.ipynb

Performance Evaluation:
Accuracy: The model performance varied based on the hyperparameters. Generally, Adam optimizer outperformed SGD, and larger filter sizes with moderate regularization performed better.
Confusion Matrix: The model made errors in classifying similar clothing items, like distinguishing between a shirt and a t-shirt.
Loss Curve: Adam showed faster convergence compared to SGD, and models with larger filters tended to overfit slightly.

My Comments:
Adam consistently outperforms SGD across all settings.

Future Improvements:
Consider adding Dropout(0.5) after dense layers to test regularization effects.

Limitations:
1.Training time increases significantly with larger filter sizes and higher regularization.
2. Onlt basic hyperparaemeter tuning was used. Bayesian classification would give better results.
