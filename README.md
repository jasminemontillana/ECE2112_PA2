# ECE2112_PA2

Created by: Jasmine Marie P. Montillana | 2ECE-B

This repository contains the completed Programming Assignment 2 for ECE2112. The project cover array creation , reshaping, statistical computations, vectorized operations,Boolean indexing, and saving arrays to '.npy' files usig NumPy. 

## A. Reproducible Normalization Problem

**Objective:** Create a reproducible random 55 integer ndarray named 'X' seeded with `2112` and normalize the complete array using `Z = (X - x¯)/σ`


**Key functions and methods used in this problem:**
`np.random.seed(2112)`: Sets the random seed to ennsure reproducoibility across runs.

`np.random.randint(10, 101, size =(5,5))`: Generates a 5x5 matrix of random integers from 10 to 100.

`X.mean()` and `X.std()` computes the overall mean and standard deviation of the matrix.

Vectorized Operations: Normalizes the elements without using Python loop.

`np.save('X_normalized.npy', 'X_normalized')`: Saves the array output as an `.npy`file.

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


## B. Cubes Divisible by 4 Problem

**Objective:** Create the first 100 positive integers, cube every element, reshape the result into a 10x10 ndarray named `C`, and filter elements divisible by 4 using Boolean indexing.

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


## C. Above-Mean Squares Problem

**Objective:** Create a 6x6 ndarray named `S` containifn the squares of the first 36 posiitive integers, compute the matrix mean, and select elements stricly greater than the mean.

**Key functions and methods used in this problem:**

`np.arange(1,37)`: Generates an array containing positive integers from 1 to 36.

`np.power(S,2)`: Squares each element in the input array.

`.reshape(6,6)`: Converts the array into a 6x6 matrix structure.

Boolean filtering (`S[S > S_mean]`): Selects elemets stricly greater than the calculated mean.

`np.save('above_mean.npy', above_mean)`: Saves the array output as an `.npy` file.

**Below is the complete Python code implementation for this function:**

```
S = np.arange(1,37)
S = np.power(S,2)

S_mean = S.mean()
above_mean = S[S > S_mean]

print(S)
print(S_mean)
print(above_mean)
print(above_mean.shape)

np.save('above_mean.npy', above_mean)
```

**Expected Output:** A 1D array containing 15 selected elements, starting at 484 and ending at 1296.


README File version History;

September 1, 2026 - Initial Commit
September 3, 2026 - Updated and Finished
