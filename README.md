# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Input the augmented matrix: Read the number of variables n and then input the elements of the augmented matrix (coefficients and constants) into a 2D array a.

2.Perform forward elimination: Modify the matrix to make it upper triangular by eliminating elements below the main diagonal using Gaussian elimination.

3.Back substitution: Solve for the variables starting from the last row and move upwards, using the upper triangular matrix to compute the values of x[i].

4.Output the solution: Print the values of the variables X0, X1, ..., Xn-1 with two decimal precision.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Yuvaram S
RegisterNumber:24900232
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
        sys.exit("Divide by zero detected!")
    
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
            
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
        x[i]=a[i][n]
        
        for j in range(i+1,n):
            x[i]=x[i]-a[i][j] * x[j]
            
        x[i]=x[i]/a[i][i]
for i in range (n):
    print("X%d = %0.2f" %(i,x[i]) ,end=" ")
*/
```

## Output:
![gaussian elimination]()
![Screenshot 2024-11-28 213146](https://github.com/user-attachments/assets/512218f9-6023-48cf-b41d-792427259938)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

