# *Course 401 Python, Entry 13: Linear Regressions

**Can you explain the basic concept of linear regression and its purpose in the context of machine learning and data analysis?**

Linear regression takes a set of data and seeks to find the best fit line in that data. The idea is to find a pattern. In machine learning and data analysis this is the core principle. The goal is to seek a strong correlation with some model. This could have predictive value. The basic formula with one dependent and one independent variable is `y = c + b*x`, y = estimated dependent variable score, c = constant, b = regression coefficient, and x = independent variable rating.

**Describe the process of implementing a linear regression model using Python’s Scikit Learn library, including the necessary steps and functions.**

Taken from [https://www.activestate.com/resources/quick-reads/how-to-run-linear-regressions-in-python-scikit-learn/](https://www.activestate.com/resources/quick-reads/how-to-run-linear-regressions-in-python-scikit-learn/)

```
# Import the packages and classes needed in this example:
import numpy as np
from sklearn.linear_model import LinearRegression

# Create a numpy array of data:
x = np.array([6, 16, 26, 36, 46, 56]).reshape((-1, 1))
y = np.array([4, 23, 10, 12, 22, 35])

# Create an instance of a linear regression model and fit it to the data with the fit() function:
model = LinearRegression().fit(x, y) 

# The following section will get results by interpreting the created instance: 
# Obtain the coefficient of determination by calling the model with the score() function, then print the coefficient:
r_sq = model.score(x, y)
print('coefficient of determination:', r_sq)

# Print the Intercept:
print('intercept:', model.intercept_)

# Print the Slope:
print('slope:', model.coef_) 

# Predict a Response and print it:
y_pred = model.predict(x)
print('Predicted response:', y_pred, sep='\n')
```

This also matches well with what was on realpython.

**What is the purpose of splitting the dataset into train and test sets, and how does this contribute to the evaluation of a machine learning model’s performance?**

The purpose of train test split testing is to simulate how a model weould perform with new data. The idea is to take some data and split the data into training data and testing data, which will be used to enhance the model. The reason for splitting is to ensure that the model can handle new data, rather than just work well with that set, which can result in overfitting. A good split for training vs testing is said to be 75 25 respectively.

## Things I want to know more about

How complicated can relationships be model to, beyond linear?
