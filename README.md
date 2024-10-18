# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: BALASUBRAMANIAM.L
RegisterNumber:  24901213
*/
import numpy as np
import matplotlib.pyplot as plt

# Input for X and Y as arrays
X = np.array(eval(input("Enter the values for X (as a list): ")))
Y = np.array(eval(input("Enter the values for Y (as a list): ")))

# Calculating the mean of X and Y
X_mean = np.mean(X)
Y_mean = np.mean(Y)

# Initializing numerator and denominator for the slope calculation
num = 0
denom = 0

# Calculating the slope (m)
for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    denom += (X[i] - X_mean) ** 2
m = num / denom

# Calculating the intercept (b)
b = Y_mean - m * X_mean

# Predicting Y values using the linear regression equation
Y_predicted = m * X + b

# Output the predicted values
print("Predicted Y values:", Y_predicted)

# Plot the original data points
plt.scatter(X, Y)

# Plot the linear regression line
plt.plot(X, Y_predicted, color='red')

# Output the slope and intercept
print("Slope (m):", m)
print("Intercept (b):", b)

# Display the plot
plt.show()
```

## Output:
![Screenshot 2024-10-18 090610](https://github.com/user-attachments/assets/a259cbec-6600-4442-91b8-2f128d863614)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
