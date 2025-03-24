Experiment 3
WAP to implement a three-layer neural network using Tensor flow library (only, no keras) to classify MNIST handwritten digits dataset. Demonstrate the implementation of feed-forward and back-propagation approaches.


*Model Description-*

This is a three-layer neural network built using TensorFlow (without Keras) to classify handwritten digits from the MNIST dataset. The model follows a feed-forward and backpropagation approach. Here’s how it works step by step:

1. **Loading the Data**
The MNIST dataset consists of images of handwritten digits (0-9).

Each image is 28x28 pixels but is flattened into a 1D array of 784 pixels.

The pixel values are normalized (scaled between 0 and 1) to make training more efficient.

The labels (0-9) are converted to one-hot encoding, meaning each number is represented as a vector (e.g., 3 becomes [0, 0, 0, 1, 0, 0, 0, 0, 0, 0]).

2. **Defining the Neural Network Structure**
This is a three-layer network:

Input Layer: 784 neurons (one for each pixel).

Hidden Layer 1: 128 neurons (uses the sigmoid activation function).

Hidden Layer 2: 64 neurons (also uses sigmoid activation).

Output Layer: 10 neurons (one for each digit 0-9, uses softmax).

Weights and biases are initialized randomly for each layer.

3. **Feed-Forward Process**
The data is passed through the first hidden layer:
Layer 1 Output=sigmoid(Input×𝑊1+𝐵1)

Then it passes through the second hidden layer:
Layer 2 Output=sigmoid(Layer 1 Output×𝑊2+𝐵2)


Finally, it reaches the output layer, which gives the predicted digit:
Output=Layer 2 Output×𝑊3+𝐵3


4. **Loss Calculation**
The model compares its predictions with the actual labels using cross-entropy loss.

If the prediction is far from the correct label, the loss is high; if it is close, the loss is low.

5. **Backpropagation and Optimization**
The model adjusts the weights using Adam Optimizer.

It works by minimizing the loss and updating the weights based on errors.

6. **Training the Model**
The training process runs for 20 epochs (iterations over the dataset).

Each epoch, data is processed in small batches of 100 images (batch size = 100).

After each epoch, the training loss and accuracy are printed.

7. **Evaluating the Model**
After training, the model's accuracy is tested on unseen data (test set).

The final train accuracy and test accuracy are displayed.

**Expected Results**
The training accuracy should be above 95%.

The test accuracy should be around 90-95% (since the model has never seen test data before).
