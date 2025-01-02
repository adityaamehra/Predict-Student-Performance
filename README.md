# Student Grade Prediction using Multiple Linear Regression

This project implements a multiple linear regression model to predict a student's grade based on several input features, including **Socioeconomic Score**, **Study Hours**, **Sleep Hours**, and **Attendance (%)**. The model is trained using a dataset that contains these input features along with the corresponding grades.

## Problem Statement

The goal of this project is to create a predictive model that estimates the grades of students based on the following features:
- **Socioeconomic Score**: A numerical value representing the socioeconomic background of the student.
- **Study Hours**: The total number of hours a student has studied.
- **Sleep Hours**: The number of hours the student sleeps on average.
- **Attendance (%)**: The percentage of classes attended by the student.

The model uses **multiple linear regression** to learn the relationship between these input features and the target variable (Grades) and can be used to predict the grade of a student for unseen data.

## Features

- **Socioeconomic Score**: A numeric value that reflects the socioeconomic background of the student, which may influence their academic performance.
- **Study Hours**: The number of hours the student spends studying, which is expected to have a direct correlation with grades.
- **Sleep Hours**: The amount of sleep the student gets, which can affect cognitive function and academic performance.
- **Attendance (%)**: The percentage of classes the student attends, which is a factor in determining their overall understanding of the course material.

## Approach

### 1. Data Preprocessing
- **Normalization**: The features (Study Hours, Sleep Hours, Attendance, Socioeconomic Score) are normalized to have zero mean and unit variance to ensure that the gradient descent converges efficiently.

### 2. Model: Multiple Linear Regression
- A multiple linear regression model is used to find the optimal coefficients (`theta`) for the relationship:
  \[
  \text{Grades} = \theta_0 + \theta_1 \times \text{Socioeconomic Score} + \theta_2 \times \text{Study Hours} + \theta_3 \times \text{Sleep Hours} + \theta_4 \times \text{Attendance}
  \]
  - **Training**: The model is trained using gradient descent, minimizing the cost function (Mean Squared Error).
  
### 3. Prediction
- After training the model, the learned coefficients are used to predict a student's grade based on their feature values.

## Evaluation

- The performance of the model is evaluated by plotting the cost function against the number of iterations and monitoring the convergence of the gradient descent.
- The final model is used to predict the grade of a student based on their input features.

## Requirements

- `numpy`: For numerical computations.
- `matplotlib`: For visualizations.
- `pandas`: (Optional) If you plan to use data from CSV files and perform more advanced data manipulation.

## Steps to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/adityaamehra/student-grade-prediction.git
   ```
2. Install dependencies:
   ```bash
   pip install numpy matplotlib
   ```
3. Run the Python script to train the model and make predictions:
   ```bash
   python grade_prediction.py
   ```

## Example Output

- The model will output the final computed values for `theta` (model parameters) and plot the cost function's convergence over time. After training, you can input a student's features and get a predicted grade.

## Future Improvements

- **Feature Engineering**: More features could be added to the model, such as student participation in extracurricular activities, parental involvement, etc.
- **Model Tuning**: Explore different learning rates for gradient descent and experiment with other optimization techniques.
- **Cross-validation**: Implement k-fold cross-validation to better estimate model performance and avoid overfitting.
