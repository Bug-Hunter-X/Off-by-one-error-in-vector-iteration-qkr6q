# Off-by-One Error in Vector Iteration

This repository demonstrates a common off-by-one error in C++ when iterating over a vector. The error arises from an incorrect loop condition that attempts to access an element beyond the vector's bounds, leading to undefined behavior.

## Problem

The provided code iterates through a vector using a `for` loop. However, the loop condition `i <= vec.size()` is incorrect.  Vectors are zero-indexed, meaning the valid indices range from 0 to `vec.size() - 1`. Accessing `vec[vec.size()]` results in an out-of-bounds access.

## Solution

The solution involves correcting the loop condition to `i < vec.size()`. This ensures that the loop iterates only through valid indices.