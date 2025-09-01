# Programming Assignment 2

This repository contains my solutions for Programming Assignment 2.

## Table of Contents
Normalization Problem: https://github.com/supremoace/BALINDONG_2ECEB_ECE2112/blob/main/README.md#normalization-problem

Divisible by 3 Problem: https://github.com/supremoace/BALINDONG_2ECEB_ECE2112/blob/main/README.md#divisible-by-3-problem

## Programming Assignments

PA2: https://github.com/supremoace/BALINDONG_2ECEB_ECE2112/blob/main/PA2.ipynb

### Programming Assignment 2
#### Normalization Problem
In this project, we are tasked to create a 5x5 random integer array, save it, and normalize it.

1. I started by generating a 5x5 array of random integers from 1 to 100 and saving it to a `.npy` file.
```python
import numpy as np

X = np.random.randint(1, 101, size=(5, 5))  # create a random 5x5 array
print("Original 5x5 random array X:")
print(X)

np.save("X_normalized.npy", X)  # save the array to a .npy file
```

2. Then, I loaded the array and performed normalization.
```python
original_arr = np.load('X_normalized.npy')  # load the saved array

X_normalized = (X - X.mean()) / X.std()  # normalize

print("The original Array is: \n", original_arr)
print("The normalized Array is: \n", X_normalized)
```

#### Divisible by 3 Problem

In this project, we are tasked to create the squares of the first 100 integers, reshape them into a 10x10 array, and find all elements divisible by 3.

I first created an array of integers from 1 to 100, squared them, and reshaped into 10x10.
```python
import numpy as np

integers = np.arange(1, 101)  # create array of integers 1 to 100
squares = integers ** 2       # square them
A = squares.reshape(10, 10)   # reshape into 10x10

print("Squares of first 100 positive integers:")
print(A)
```

2. Then, I extracted all elements divisible by 3 and saved them into a .npy file.
```python
div_by_3 = A[A % 3 == 0]  # elements divisible by 3

np.save("div_by_3.npy", div_by_3)  # save results
Num_div_by_3 = np.load("div_by_3.npy")  # reload file

print("\nElements in A that are divisible by 3: \n", Num_div_by_3)
print(f"\nNumber of elements divisible by 3: {len(Num_div_by_3)}")
```
