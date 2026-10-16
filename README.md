# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start. Read number of unknowns n and augmented matrix a[n][n+1]. Initialize solution array x.
2. Forward Elimination: For i=0 to n-1, if a[i][i]==0, swap with below row. For j=i+1 to n-1, calculate ratio = a[j][i]/a[i][i] and eliminate: a[j][k] = a[j][k] - ratio*a[i][k] for all k.
3. Backward Substitution: Set x[n-1] = a[n-1][n]/a[n-1][n-1]. For i=n-2 down to 0, x[i] = a[i][n] - Σ a[i][j]*x[j] (j=i+1 to n-1), then x[i] = x[i]/a[i][i].
4. Display the solutions X0, X1,... Xn-1 up to 2 decimal places. Stop.

## Program:
### Program to solve a matrix using Gaussian elimination without partial pivoting.
### developed by:DHATSHINI.P 
### RegisterNumber: 26010141

### import os
### os.environ["OPENBLAS_NUM_THREADS"]="1"
### import numpy as np
### import sys
### n = int(input())
### a = np.zeros((n,n+1))
### X = np.zeros(n)
### for i in range(n):
###  for j in range(n+1):
###    a[i][j] = float(input())
### 
### for i in range(n):
###    for j in range(i+1,n):
###       ratio = a[j][i]/a[i][i]
###         
###       for k in range(n+1):
###         a[j][k] = a[j][k] - ratio*a[i][k]

### X[n-1] = a[n-1][n]/a[n-1][n-1]

### for i in range(n-2,-1,-1):
###   X[i] = a[i][n]
###   for j in range(i+1,n):
###       X[i] = X[i]-a[i][j]*X[j]
###   X[i] = X[i]/a[i][i]
### for i in range(n):
###     print('X%d = %0.2f'% (i,X[i]),end=' ')

## Output:
<img width="1106" height="691" alt="Screenshot 2026-10-16 125446" src="https://github.com/user-attachments/assets/0b5860da-920b-446d-96f2-056148cf0df8" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

