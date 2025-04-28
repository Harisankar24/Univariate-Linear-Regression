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
import matplotlib.pyplot as plt
X = [1, 2, 3, 4, 5]
Y = [2, 4, 5, 4, 5]
mean_X = sum(X) / len(X)
mean_Y = sum(Y) / len(Y)
numerator = sum((X[i] - mean_X) * (Y[i] - mean_Y) for i in range(len(X)))
denominator = sum((X[i] - mean_X)**2 for i in range(len(X)))

m = numerator / denominator

b = mean_Y - m * mean_X

print(f"The equation of the best fit line is: Y = {m:.2f}X + {b:.2f}")

plt.scatter(X, Y, color='blue', label='Data points')

Y_pred = [m * x + b for x in X]
plt.plot(X, Y_pred, color='red', label='Best fit line')

plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression')
plt.legend()
plt.show()





```
## Output
![image](https://github.com/user-attachments/assets/e4a358f4-5e76-41e1-a1fa-362e4123e660)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
