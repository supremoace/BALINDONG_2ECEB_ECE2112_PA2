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
