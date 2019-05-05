# SparseMatrixDicts

## Quick start

This package creates a sparse matrix as Dictionary.
You can convert the dictionary to a SparseCSC matrix or a dense matrix.
It is useful when the nonzero elements randomly occur and you can not prepare the sparse storage before you see the actual elements.

```
using SparseMatrixDicts
n = 5
A = SparseMatrixDict(n,n)  # default={Float64,Int}
A[1,1] = 2.0
A[2,5] = 2.0

# convert to dense matrix
dA = Matrix(A)

# convert to sparse matrix CSC
sA = SparseMatrixCSC(A)

# make a symmetric sparse matrix
symA = Symmetric(SparseMatrixCSC(A),:U)  # :U for upper
```
