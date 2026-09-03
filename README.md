	# ECE2112_PA2

Created by: Jasmine Marie P. Montillana | 2ECE-B

This repository contains the completed Programming Assignment 2 for ECE2112. The project cover array creation , reshaping, statistical computations, vectorized operations,Boolean indexing, and saving arrays to '.npy' files usig NumPy. 

## A. Reproducible Normalization Problem

Objective: Create a reproducible random 55 integer ndarray named 'X' seeded with `2112` and normalize the complete array using xxxx


**Key functions and methods used in this problem:**
`np.random.seed(2112)`: Sets tje andom seed to ennsure reproducoibility across runs xxxx

`np.random.randint(10, 101, size =(5,5))`: Generates a 5x5 matrix of random integers from 10 to 100 xxxx

`X.mean()` and `X.std()` computes the overall mean and standard deviation of the matrix xxxx

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
**Expected Output:** A 5x5 normalized matrix with a mean of approximately 0, and a standard deviation of 1.


## Cubes Divisible by 4 Problem

Objective: Create the first 100 positive integers, cube every element, reshape the result into a 10x10 ndarray named `C`, and filter elements divisible by 4 using Boolean indexing.

**Key functions and methods used in this problem:**

`np.arange(1,101)`: Generates an array containing positve integers from 1 to 100.

`np.power(a, 3)`: Computes the cube of each element in the array.

`.reshape(10,10)`: Reshapes the 1D array into a 2D matrix of shape 10x10.

Boolean Indexing (`c[c % 4 == 0]`): Filters elementss that satisfy the divisibility condition.

`np.save('div_by_4.npy', div_by_4)`: Saves the array output as an `.npy` file.

**Below is the complete Python code implementation for this function.**

```
c = np.arange(1,101)
c = np.power(c,3)
c = c.reshape(10,10)

div_by_4 = c[c % 4 == 0]

print(div_by_4)
print(div_by_4.shape)
print(len(div_by_4))

np.save('div_by_4.npy', div_by_4)
```
**Expected Output:** A 1D arry containing 50 selected elements, starting at 8 and ending at 1000000.



