# Project 1: Linear Regression – Analytical & Numerical Methods
This repository contains a Jupyter Notebook implementation of linear regression using both analytical and numerical approaches. The project demonstrates how to train, validate, and test a regression model on given datasets while evaluating model performance.

## 📌 Project Overview
The project is divided into two main parts:

### Part 1: Analytical Method
- Implements linear regression with the closed-form solution.
- Derives weights
- using the normal equation.
- Evaluates the model using Root Mean Square Error (RMSE).
- Visualizes fitted regression lines for training, validation, and test sets.

### Part 2: Numerical Method
- Uses gradient descent to optimize regression weights.
- Iteratively updates parameters to minimize error.
- Compares results with the analytical solution.
- Plots error convergence curves and regression lines.

## 📂 Datasets
The project uses three datasets (CSV files) provided separately:

    Dataset_1_train.csv – Training data
    Dataset_1_valid.csv – Validation data
    Dataset_1_test.csv – Test data

Each dataset contains pairs of (x,y) values for regression.

## 🛠️ Technologies Used
  
    Python 3
    NumPy (numerical operations, linear algebra)
    Pandas (data handling)
    Matplotlib (visualization)

## 🚀 How to Run

    git clone https://github.com/your-username/project1-linear-regression.git
    cd project1-linear-regression

Install dependencies:

    pip install numpy pandas matplotlib

Open the notebook in Jupyter or Google Colab:

    jupyter notebook Project1.ipynb
    Upload the datasets when prompted (train, validation, test CSV files).

## 📊 Expected Outputs
- Plots of regression lines overlaid on training, validation, and test datasets.
- RMSE values for each dataset.
- Convergence curve of gradient descent (Part 2).
