# Petrol-consumption-prediction-with-PyTorch

This project predicts the gas consumption (in millions of gallons) across 48 US states based on the following features:

- Gas taxes (in cents)
- Per capita income (dollars)
- Paved highways (in miles)
- Proportion of the population with a driver’s license
  
We use a neural network built with PyTorch to train on the dataset and make predictions. After training the model, we use it to predict the gas consumption for a given observation.

**Dataset**

The dataset can be accessed here.

**Features:**

- Petrol_tax: Gas taxes in cents.
- Average_income: Per capita income in dollars.
- Paved_Highways: Paved highways in miles.
- Population_Driver_licence(%): Percentage of the population with a driver's license.
- Petrol_Consumption: Gas consumption in millions of gallons (Target).
  
**Project Overview**

- **Step 1: Data Preparation**
Load the dataset and check the columns.


Separate the features and target:

Features: Petrol_tax, Average_income, Paved_Highways, and Population_Driver_licence(%).

Target: Petrol_Consumption.

- **Step 2: Building the Neural Network**
  
A simple feedforward neural network is used, consisting of:

- 4 input features
- 3 fully connected layers with ReLU activation
- 1 output layer for the regression task
- 
The architecture is as follows:

- Input Layer: 4 neurons (one for each feature)
- Hidden Layers: 128, 64, 32 neurons
- Output Layer: 1 neuron for predicting gas consumption
  
**Step 3: Training the Model**

Loss Function: Mean Squared Error (MSE)

Optimizer: Adam Optimizer

Training Loop: The model is trained for 1000 epochs, and the loss is monitored throughout.

**Step 4: Evaluating the Model**

We evaluate the trained model using the Mean Absolute Error (MAE) and Mean Squared Error (MSE) metrics on the test set.

**Step 5: Visualizing the Loss**

The loss is plotted across the epochs to observe the model's learning process.

**Results**

- Mean Absolute Error: 124.16
- Mean Squared Error: 17472.64
- Final Prediction on new data: 527.7 million gallons

**Step 6: Making Predictions**

After training, the model is used to make predictions on unseen data. Specifically, the model predicts the gas consumption for the following new observation:

- Gas tax: 8.5 cents
- Average income: $4550
- Paved highways: 1980 miles
- Population with license: 75%
  
**Final Prediction:**
The model predicts a gas consumption of 527.7 million gallons for the given observation.

**License**
This project is licensed under the MIT License - see the LICENSE file for details.
