# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.tart the program.
2.import numpy,import sys.
3.Use gaussian solving methods
4.Display the values.
5.End the program
## Program:
```
'''Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: JEEVITHA S
RegisterNumber: 212222100016
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
     for j in range(n+1):
         a[i][j]=float(input())
for i in range(n):
     if a[i][i]==0.0:
         sys.exit('Divide by zero detected')
     for j in range(i+1,n):
         retio=a[j][i]/a[i] [i]
         for k in range(n+1):
             a[j][k]=a[j][k]-retio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
```    
## Output:

![image](https://github.com/Jeevithha/Gaussian/assets/123623197/661718db-9408-49ae-817f-7b4cad8728b6)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

