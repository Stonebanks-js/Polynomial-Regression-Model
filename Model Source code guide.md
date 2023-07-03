# Polynomial-Regression-Model
A model that tests dataset based upon the working of Polynomial regression
--- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 Importing the necessary libraries:

numpy (as np): A library for numerical operations in Python.
matplotlib.pyplot (as plt): A library for creating visualizations in Python.
pandas (as pd): A library for data manipulation and analysis in Python.

--- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Importing the dataset:

The code assumes that there is a file named 'Position_Salaries.csv' at the specified path '/home/aradhya/Documents/Regression Models /Position_Salaries.csv'.
The data is read using the read_csv function from pandas, and the independent variable (X) and dependent variable (y) are extracted from the dataset.

--- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Splitting the data into training and test sets:

The train_test_split function from scikit-learn is used to split the data into training and test sets.
The test set size is set to 20% (test_size=0.2) of the entire dataset.
The random_state parameter ensures reproducibility of the split.

--- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


Training the polynomial regression model:

The PolynomialFeatures class from scikit-learn is used to transform the original features (X) into polynomial features of the desired degree (4 in this case).
The transformed features are stored in X_poly using the fit_transform method.
The LinearRegression class from scikit-learn is used to create a regression object named regressor.
The fit method is called to train the model using the transformed features (X_poly) and the target variable (y_train).

--- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Predicting the test set results:

The predict method of the regressor object is used to predict the salaries for the test set (X_test) after transforming it using poly_reg.transform.

--- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The predicted values (y_pred) are printed along with the actual values (y_test) using np.concatenate.
Evaluating the model performance:

The r2_score function from scikit-learn is used to compute the coefficient of determination (R-squared) between the predicted values (y_pred) and the actual values (y_test).
The R-squared score is printed.
