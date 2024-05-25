# Matrix Operations and Gaussian Elimination

This repository contains Python scripts for performing various matrix operations and Gaussian elimination. The provided scripts are `hw03prog.py` and `gauss.py`.

## Files

- `hw03prog.py`: Contains functions for matrix operations such as checking equality, matrix-vector multiplication, creating matrices from vectors, and verifying the consistency of augmented matrices.
- `gauss.py`: Contains functions related to Gaussian elimination, including swapping rows, checking for inconsistent rows, and performing the elimination and back substitution phases.

## Functions in `hw03prog.py`

1. **mat_eq(a, b)**: Checks if two matrices are equal.
2. **vec_eq(u, v)**: Checks if two vectors are equal.
3. **mat_vec_mul(a, v)**: Multiplies a matrix with a vector.
4. **mat_of_vecs(vs)**: Creates a matrix from a list of column vectors.
5. **vecs_of_mat(a)**: Creates a list of column vectors from a matrix.
6. **add_col(a, v)**: Adds a column to a matrix.
7. **is_consistent_aug(a)**: Checks if an augmented matrix is consistent.

## Functions in `gauss.py`

1. **swap_rows(a, i, j)**: Swaps rows \(i\) and \(j\) in matrix \(a\).
2. **is_inconsistent_row(r)**: Checks if a row is inconsistent.
3. **num_of_rows(a)**: Returns the number of rows in a matrix.
4. **leftmost_nonzero_index(a, row_index)**: Finds the leftmost non-zero entry in a row.
5. **zero_in_pivot_column(a, lower_row_index, pivot_row_index, pivot_col_index)**: Eliminates the entry in the pivot column for the lower row.
6. **scale_to_one_in_pivot_column(a, pivot_row_index, pivot_col_index)**: Scales the pivot row so that the pivot entry is 1.
7. **elimination_phase(a)**: Converts a matrix into echelon form.
8. **back_substitution_phase(a)**: Converts a matrix in echelon form into one in reduced echelon form.
9. **gaussian_elimination(a)**: Converts a matrix into reduced echelon form.

## Usage

1. Import the necessary functions from the scripts.
2. Use the functions as required for matrix operations or Gaussian elimination.

### Example

```python
import numpy as np
from hw03prog import mat_eq, mat_vec_mul
from gauss import gaussian_elimination

# Example matrix and vector
A = np.array([[1, 2], [3, 4]])
v = np.array([5, 6])

# Matrix-vector multiplication
result = mat_vec_mul(A, v)
print("Matrix-Vector Multiplication Result:", result)

# Gaussian Elimination
B = np.array([[2, 1, -1, 8],
              [-3, -1, 2, -11],
              [-2, 1, 2, -3]], dtype=float)
gaussian_elimination(B)
print("Reduced Echelon Form:", B)
```

## License

This project is licensed under the MIT License.
```