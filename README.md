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

import numpy as np
import matplotlib.pyplot as plt

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

b1 = np.sum((x - np.mean(x)) * (y - np.mean(y))) / np.sum((x - np.mean(x)) ** 2)
b0 = np.mean(y) - b1 * np.mean(x)

y_pred = b0 + b1 * x

print("Slope:", round(b1, 2))
print("Intercept:", round(b0, 2))
print("Predicted values:", np.round(y_pred, 2))

plt.scatter(x, y, label="Actual Data")
plt.plot(x, y_pred, color="red", label="Regression Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression")
plt.legend()
plt.grid(True)
plt.show()

```

## Output:
<img width="1101" height="701" alt="Screenshot 2026-10-23 085819" src="https://github.com/user-attachments/assets/c2d9221d-eaba-424d-ba17-651e17e301c2" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
