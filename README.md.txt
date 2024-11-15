Predicting Tensile Strength of 3D Printed ABS Using Machine Learning

Overview
This project predicts the tensile strength of additively manufactured ABS plastic using three machine learning models:

Linear Regression
XGBoost Regressor
PyTorch Neural Network
The dataset, originally containing 50 entries, was augmented to 1,050 entries to improve model performance.

Dataset
Source: Kaggle - https://www.kaggle.com/code/semihakmese/tensile-test-application-using-by-deep-learning-a/input?select=data.csv
Original Size: 50 entries
Augmented Size: 1,050 entries
Data Augmentation
To expand the small dataset and preserve the original distribution,  a synthetic dataset was generated with 1,000 additional rows based on the original data. The augmentation process involved:

Random Sampling with Gaussian Noise: New data points were created by adding Gaussian noise to the original data, introducing slight variations while maintaining the underlying patterns.
Purpose: This method effectively preserves the original distribution and improves the models' ability to generalize.

Features Used
layer_height
wall_thickness
infill_density
nozzle_temperature
print_speed
fan_speed
These features are key printing parameters affecting the tensile strength of ABS prints.

Models and Results
Linear Regression
Training Set:
R² Score: 0.6329
RMSE: 5.3313
Test Set:
R² Score: 0.6242
RMSE: 5.4088
The model confirms a linear relationship between features and tensile strength, explaining about 63% of the variance.

XGBoost Regressor
Training Set:
R² Score: 0.99
RMSE: 0.70
Test Set:
R² Score: 0.97
RMSE: 1.54
XGBoost captures complex relationships with high accuracy, providing the best performance among the models.

PyTorch Neural Network
Training Set:
R² Score: 0.9518
RMSE: 1.9320
Test Set:
R² Score: 0.9519
RMSE: 1.9343
The neural network effectively models nonlinear patterns, showing strong performance.

Conclusion
Linear Regression demonstrates a linear relationship but may not capture all complexities.
XGBoost Regressor provides the highest accuracy and is suitable for predicting tensile strength.
PyTorch Neural Network also yields high accuracy, effectively modeling complex patterns.
