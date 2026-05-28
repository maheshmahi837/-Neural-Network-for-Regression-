# Neural Network for Regression using PyTorch

## Overview

This repository contains the implementation of a Fully Connected Neural Network (FCNN) for regression tasks using PyTorch. The project was developed as part of the **AI61002: Deep Learning Foundations and Applications** course assignment.

The objective of this project is to build an end-to-end deep learning pipeline for predicting continuous output variables, including data preprocessing, model training, evaluation, visualization, and inference.

---

## Project Objectives

* Split the dataset into training, validation, and testing partitions
* Design and implement a Fully Connected Neural Network (FCNN)
* Train the model using stochastic gradient descent (SGD)
* Apply learning rate scheduling for stable convergence
* Visualize training performance using TensorBoard
* Evaluate the model using Mean Squared Error (MSE)
* Compare predictions with ground truth values using scatter plots
* Save and reload trained models for inference

---

## Technologies Used

* Python
* PyTorch
* NumPy
* Matplotlib
* TensorBoard
* Scikit-learn
* Jupyter Notebook

---

## Project Structure

```bash
├── assignment_1.ipynb          # Jupyter Notebook implementation
├── assignment_1.py             # Python script implementation
├── saved_models/               # Trained model checkpoints
├── runs/                       # TensorBoard logs
├── plots/                      # Generated visualizations
├── README.md                   # Project documentation
```

---

## Dataset Processing

The dataset was divided into:

* **70% Training Set**
* **15% Validation Set**
* **15% Test Set**

PyTorch `DataLoader` objects were used for efficient batch-wise data loading during training and evaluation.

---

## Model Architecture

The project uses a Fully Connected Neural Network (FCNN) designed specifically for regression problems.

### Key Features

* Multiple hidden layers
* ReLU activation for hidden layers
* Linear activation at output layer
* Hyperparameter tuning through experimentation
* Trainable parameter analysis

---

## Training Details

### Optimizer

* Stochastic Gradient Descent (SGD)

### Loss Function

* Mean Squared Error Loss (MSELoss)

### Additional Techniques

* Learning rate scheduling
* Validation monitoring
* Overfitting prevention
* Batch size experimentation

---

## TensorBoard Visualization

TensorBoard was integrated to monitor:

* Training loss
* Validation loss
* Training progression across epochs

### Run TensorBoard

```bash
tensorboard --logdir=runs
```

---

## Model Saving and Loading

The trained model is saved after training and can be reloaded later for inference and evaluation.

```python
torch.save(model.state_dict(), "model.pth")
```

```python
model.load_state_dict(torch.load("model.pth"))
```

---

## Evaluation

The trained model was evaluated on the test dataset using:

* Mean Squared Error (MSE)
* Prediction vs Ground Truth scatter plots

The scatter plots provide a visual comparison between actual target values and predicted outputs for both regression variables.

---

## Results

The model achieved stable convergence during training and demonstrated effective regression performance on unseen test data.

Key observations:

* Validation monitoring helped reduce overfitting
* Learning rate scheduling improved convergence stability
* Scatter plots showed reasonable prediction alignment with ground truth values

---

## How to Run

### Clone the Repository

```bash
git clone <your-repository-link>
cd <repository-folder>
```

### Install Dependencies

```bash
pip install torch torchvision numpy matplotlib scikit-learn tensorboard
```

### Run the Notebook

```bash
jupyter notebook
```

Open:

```bash
assignment_1.ipynb
```

---

## Learning Outcomes

This project helped in understanding:

* Neural network design for regression tasks
* Deep learning workflow in PyTorch
* Training optimization techniques
* Hyperparameter tuning
* TensorBoard visualization
* Model evaluation methods
* End-to-end machine learning experimentation

---

## Assignment Reference

This implementation follows the requirements specified in the AI61002 Assignment 1 guidelines.

---

## Author

Mahesh Kusireddy

AI61002 - Deep Learning Foundations and Applications
Indian Institute of Technology Kharagpur
