# EXP. NO: 03

# DATE: 


# <p align = "center"> Marginal distributions and correation coefficient </p>
  

# Aim : 

To find marginal distributions and correation coefficient of joint probability mass funcition of two dimensional random variables

![image](https://user-images.githubusercontent.com/104613195/168222062-bb7dec1f-f115-4669-8b4c-58283af8ccf3.png)

# Software required :  

Python

# Theory:

A marginal distribution is a distribution of values for one variable that ignores a more extensive set of related variables in a dataset.
The marginal mass function for X is found by summing over the appropriate column and the marginal mass function
for Y can be found be summing over the appropriate row.

Correlation coefficients are indicators of the strength of the linear relationship between two different variables. The coefficient of correlation is measure of degree of realtionship betwen two variavbles. A linear correlation coefficient that is greater than zero indicates a positive relationship. A value that is less than zero signifies a negative relationship. Finally, a value of zero indicates no relationship between the two variables x and y.  



# <br>Procedure :
![image](https://user-images.githubusercontent.com/104613195/168220332-09383cb4-a7ac-4526-b547-fc522ca53227.png)



# Program

```python
# Developed by:Kumaran.B
# Reg no:212220230026
import math
import numpy as np
p = [[0,0.01,0.03,0.05,0.07,0.09],
    [0.01,0.02,0.04,0.05,0.06,0.08],
     [0.01,0.03,0.05,0.05,0.05,0.06],
    [0.01,0.02,0.04,0.06,0.06,0.05]]
px=np.sum(p,axis=0)
py=np.sum(p,axis=1)
x=[0,1,2,3,4,5]
ex=np.inner(x,px)
y=[0,1,2,3]
ey=np.inner(y,py)
ex2=np.inner(np.square(x),px)
ey2=np.inner(np.square(y),py)
vx=ex2-ex**2
sx=math.sqrt(vx)
vy=ey2-ey**2
sy=math.sqrt(vy)
exy=0
for i in range(4):
    for j in range(6):
        exy=exy+x[j]*y[i]*p[i][j]
cov=exy-ex*ey
r=cov/(sx*sy)
import pandas as pd
pdf_df=pd.DataFrame(p)
display(pdf_df)
print("Variance of X:\t\t\t\t",vx)
print("Variance of Y:\t\t\t\t",vy)
print("Standard deviation of X:\t\t",sx)
print("Standard deviation of Y:\t\t",sy)
print("Covariance:\t\t\t\t",cov.round(4))
print("Covariance Coefficient of Corelation:\t",r.round(4))
```
# Output : 
![Screenshot (190)](https://user-images.githubusercontent.com/75243072/168965836-65e1fd0b-1d5c-4f2c-982d-9fca4dfac315.png)

# Result:
Thus,the program is implemented on Marginal distributions and correation coefficient.

