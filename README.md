# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy package.
2.Get the input.
3. FInd gaussian elimination.
4. Print the result.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Premalatha.S
RegisterNumber: 22009393
*/
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
X=np.zeros(n)
for i in range(n):
for j in range(n+1):
a[i][j] = float(input())
for i in range(n):
if a[i][i] == 0.0:
sys.exit('Divide by zero detected!')
for j in range(i+1,n):
ratio = a[j][i]/a[i][i]
for k in range(n+1):
    a[j][k] = a[j][k]-ratio*a[i][k]
X[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
X[i] = a[i][n]
for j in range(i+1,n):
X[i] = X[i]-a[i][j]*X[j]
X[i] = X[i]/a[i][i]
for i in range(n):
print('X%d = %0.2f'%(i,X[i]),end=' ') 
```

## Output:

![image](https://user-images.githubusercontent.com/120620842/213877531-90c1a70f-b1f7-456a-93fd-1975e862197b.png)


![image](https://user-images.githubusercontent.com/120620842/213877550-93354b29-8274-4768-aa93-d68b810df061.png)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

