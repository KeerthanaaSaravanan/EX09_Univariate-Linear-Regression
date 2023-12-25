# EX-09: Implementation of Univariate Linear Regression
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
 
5.	Compute the y -intercept of the line by using the formula:


![eqn2](./eq2.jpg)  

6.	Use the slope m and the y -intercept to form the equation of the line.
7.	Obtain the straight line equation Y=mX+b and plot the scatterplot.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Program
```
'''
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: KEERTHANA S
#register number: 23013398
'''

import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Orange')
plt.plot(x,ypred,color='Blue')
plt.show()

```
<br>
<br>
<br>
<br>

## Output
![Screenshot 2023-12-25 151529](https://github.com/KeerthanaaSaravanan/EX09_Univariate-Linear-Regression/assets/145742596/d36f67b6-1369-499e-9c5b-5ad4cd78d64a)
![Screenshot 2023-12-25 151541](https://github.com/KeerthanaaSaravanan/EX09_Univariate-Linear-Regression/assets/145742596/be0d9e36-903f-40f7-a3b4-49adfe333b7e)
![Screenshot 2023-12-25 151549](https://github.com/KeerthanaaSaravanan/EX09_Univariate-Linear-Regression/assets/145742596/b7482037-a4e4-43a1-bb6c-1e0a8f82dd7e)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
