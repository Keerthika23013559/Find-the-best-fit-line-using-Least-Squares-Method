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
Developed by: KEERTHIKA M P
RegisterNumber:212223240071
*/
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)
num=0
denum=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
m=num/denum
print(m)
b=Y_mean - m*X_mean
print(b)
Y_pred=m*X+b
print(Y_pred)
plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='yellow') 
plt.show()

*/
```
## Output:
![image](https://github.com/user-attachments/assets/4482601d-7c07-4bfe-a318-4275967e9798)

![image](https://github.com/user-attachments/assets/762e2d7a-a784-42eb-a140-637575872201)

![image](https://github.com/user-attachments/assets/05db38f5-a619-4a3b-b9ba-23cc72bb839d)

![image](https://github.com/user-attachments/assets/391c9cf3-6a7d-4a1b-801f-525e03bab005)

![image](https://github.com/user-attachments/assets/a10e9dd6-aab2-4928-a861-a64d788dadbc)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
