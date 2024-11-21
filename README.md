

Matrix Inversion with Caching in R
This repository contains an implementation of a caching system for matrix inversion in R. The code leverages the concept of lexical scoping to store a matrix and its inverse, reducing redundant computations.

Features
Efficient computation of matrix inversion.
Caching mechanism to store the inverse of a matrix.
Avoids re-computation by fetching the cached inverse when applicable.
Functions
1. makeCacheMatrix
Creates a special "matrix" object that can cache its inverse.
Parameters:

x: A square invertible matrix. Default is a 3x3 random matrix.
Methods:

set(y): Sets a new matrix and resets the cached inverse.
get(): Returns the current matrix.
setslv(slv): Stores the inverse of the matrix.
getslv(): Retrieves the cached inverse.
2. cacheSolve
Computes the inverse of the matrix stored in the special "matrix" object.
Steps:

Checks if the inverse is already cached.
If cached, it returns the inverse with a message: getting inversed matrix.
If not cached, computes the inverse using the solve function, stores it in the cache, and then returns it.

How It Works
The makeCacheMatrix function creates a list of methods to store and retrieve both the matrix and its inverse.
The cacheSolve function computes the inverse of the matrix if it has not been computed or retrieves it from the cache if it has.
Prerequisites
R version 3.5 or higher.
Basic knowledge of matrices and their inverses.


