[![Build Status](https://travis-ci.org/MathieuNls/gpbt.png)](https://travis-ci.org/MathieuNls/gpbt)
[![GoDoc](https://godoc.org/github.com/MathieuNls/gpbt?status.png)](https://godoc.org/github.com/MathieuNls/gpbt)
[![codecov](https://codecov.io/gh/MathieuNls/gpbt/branch/master/graph/badge.svg)](https://codecov.io/gh/MathieuNls/gpbt)

# Go Parallel Binary Trees 

This package provides a parallel binary tree where the the *Fetch* and *Add* complexities are  *O(log(k) + log(n)/k)* where N is a the number of keys and k the number of threads.

It works by creating a root-tree where each node is the root of a sub-tree. This divides the search space by k for the *Fetch* and *Add* operation as shown below.



To fetch the key 149 (on the right most sub-tree), we first search for the floor key of 149 which gives us 150. 
Then, we look for 149 inside the sub-tree. 
