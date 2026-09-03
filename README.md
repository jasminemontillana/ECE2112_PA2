	# ECE2112_PA2

Created by: Jasmine Marie P. Montillana | 2ECE-B

This repository contains the completed Programming Assignment 2 for ECE2112. The project cover array creation , reshaping, statistical computations, vectorized operations,Boolean indexing, and saving arrays to '.npy' files usig NumPy. 

## A. Reproducible Normalization Problem

Objective: Create a reproducible random 55 integer ndarray named 'X' seeded with `2112` and normalize the complete array using xxxx


**Key functions and methods used in this problem:**
`np.random.seed(2112)`: Sets tje andom seed to ennsure reproducoibility across runs xxxx

`np.random.randint(10, 101, size =(5,5))`: Generates a 5x5 matrix of random integers from 10 to 100 xxxx

`X.mean()` and `X.std()` computes the oiverall mean and standard deviation of the matrix xxxx

Vectorized Operations: Normalizes the elements without using Python loop xxxxx

`np.save('X_normalized.npy', 'X_normalized')`: Saves the array output as an `.npy`file xxxxx.

**Below is the complete Python code implementation for this function.**
```
np.random.seed(2112)
X = np.random.randomint(10, 101, size = (5,5))

x_mean = X.mean()
x_std = X.std()

X_normalized = (X - x_mean)/x_std
print(X_normalized)
print(X_normalized.mean())
print(X_nomrmalized.std())

np.save('X_normalized.npy', X_normalized)

```
