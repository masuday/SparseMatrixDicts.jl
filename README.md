# SparseMatrixDicts

## Quick start

Creates s sparse matrix with a hash table.
It can be used as a dense matrix.

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
symA = Symmetric(SparseMatrixCSC(A),:U)  # :L for lower
```
