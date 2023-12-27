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
![eq1](https://github.com/ILAIYADEEPAN/Univariate-Linear-Regression/assets/147473334/7aa956ca-8898-4f57-ac80-1088cbd52698)

4.	Compute the y -intercept of the line by using the formula:
![eq2](https://github.com/ILAIYADEEPAN/Univariate-Linear-Regression/assets/147473334/b62857b9-9529-45bf-b22d-01cfd5928f7a)

5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Developed by : ILAIYADEEPAN . K
#Register number : 23013535
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
m=num/den
b=ymean-m*xmean
print(m,b)
ypred=m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()


```
## Output
![output 1](https://github.com/ILAIYADEEPAN/Univariate-Linear-Regression/assets/147473334/6ebaf6a9-5e4d-4c76-acd5-57df8e90d79d)
![output 2](https://github.com/ILAIYADEEPAN/Univariate-Linear-Regression/assets/147473334/df268089-0a9e-4d3f-a531-343cc91be311)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
