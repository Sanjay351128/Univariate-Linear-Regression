# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import numpy as np
import matplotlib.pyplot as plt

# Sample data (you can change this)
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

# Number of observations
n = len(x)

# Calculate slope (m) and intercept (c) using least squares formula
m = (n*np.sum(x*y) - np.sum(x)*np.sum(y)) / (n*np.sum(x**2) - (np.sum(x))**2)
c = (np.sum(y) - m*np.sum(x)) / n

print("Slope (m):", m)
print("Intercept (c):", c)

# Predicted values
y_pred = m*x + c

# Plot the data points and regression line
plt.scatter(x, y, color='blue', label="Data Points")
plt.plot(x, y_pred, color='red', label="Regression Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression using Least Squares")
plt.legend()
plt.show()

```
## Output

<img width="821" height="631" alt="image" src="https://github.com/user-attachments/assets/8d1938a5-4fdf-4965-87cd-eb705a9141be" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
