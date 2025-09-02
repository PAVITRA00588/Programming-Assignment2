# Programming Assignment 2: Lexical Scoping

This repository contains the solution for *Programming Assignment 2: Lexical Scoping* from the R Programming course.

## Files
- *cachematrix.R* – Implementation of two functions demonstrating lexical scoping and caching in R.

## Functions
- makeCacheMatrix()  
  Creates a special "matrix" object that can store its inverse using lexical scoping.  

- cacheSolve()  
  Computes the inverse of the matrix returned by makeCacheMatrix(). If the inverse has already been calculated, it retrieves the cached result instead of recalculating it.

## Concept
This assignment demonstrates:
- *Lexical scoping* in R  
- The use of *closures* to maintain state  
- Efficient computation using *caching*  

## Example
```R
source("cachematrix.R")

# Create a matrix
m <- matrix(c(1, 2, 3, 4), 2, 2)

# Create a special matrix object
cm <- makeCacheMatrix(m)

# Compute and cache the inverse
inv1 <- cacheSolve(cm)

# Retrieve the cached inverse
inv2 <- cacheSolve(cm)
