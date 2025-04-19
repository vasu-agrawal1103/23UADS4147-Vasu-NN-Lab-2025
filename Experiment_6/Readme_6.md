Description of the Model
This is a Recurrent Neural Network (RNN) model built using PyTorch to forecast daily minimum temperatures.
It takes the past 7 days' temperatures as input and predicts the temperature for the next day.
RNNs are particularly useful for time series problems because they capture sequential dependencies.
input_size=1: Only one feature (temperature).
hidden_size=64: Hidden layer dimension.
batch_first=True: Ensures the batch dimension is the first.
fc: Linear layer maps the last RNN output to the predicted temperature.
Loss: The model uses Mean Squared Error (MSE) as the loss function to measure the difference between predicted and actual temperatures.
Optimizer: Uses Adam optimizer to minimize the loss and update model weights efficiently.

Description of the code
Import Libraries
PyTorch (torch, nn): For building and training the neural network.
NumPy, Pandas: For data manipulation and preprocessing.
Matplotlib: For visualizing loss and results.
Sklearn: For scaling and evaluating the model.
Load the dataset
Loads the Daily Minimum Temperatures dataset.

Extracts the Temp column and reshapes it into a 2D array suitable for scaling.

MinMaxScaler scales the temperatures to the range [0, 1], which is important for stable and faster training of the model.


Training
This function splits the data into input-output pairs using a sliding window.
For each 7-day sequence (x), the target is the temperature on the 8th day (y).
Creates sequences and converts them into PyTorch tensors for model input.
X.shape = [samples, 7, 1], and y.shape = [samples, 1].
Forward pass: Predicts using current model.
Loss computation: MSE between predicted and actual.
Backpropagation: Updates weights using gradients.
Logs training loss every 10 epochs.

Testing
Switches model to evaluation mode.
Disables gradient computation for inference.
Predicts on test set.

Calculate MAE
Measures the average error in predicted temperatures.
Gives an intuitive sense of prediction accuracy.
Visualizes how close the model's predictions are to the real temperatures.
A useful qualitative check of model performance.


MY COMMENTS
Performance is evaluated using Mean Squared Error.
Actual vs Predicted values of temperatures is plotted.
Performance can be improved using LSTM / GRU.
the mean absolute eroor is 2.35 degree Celcius.