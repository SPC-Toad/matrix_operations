# Matrix Operations Project

This project implements various matrix operations in Python, including Gaussian elimination and other matrix manipulations.

## Project Structure

- **gauss.py**: This script contains the implementation of Gaussian elimination.
- **matrix_operation.py**: This script includes various matrix operations such as addition, subtraction, multiplication, and inversion.
- **Makefile**: This file is used to automate the build process of the project.

## Requirements

- Python 3.x

## Usage

### Running Gaussian Elimination

To run the Gaussian elimination script, execute the following command:

```bash
python gauss.py
```

### Running Matrix Operations

To run the matrix operations script, execute the following command:

```bash
python matrix_operation.py
```

### Building the Project

To build the project using the Makefile, run:

```bash
make
```

This will execute the commands specified in the Makefile to build and run the project.

## Project Details

### gauss.py

This script contains functions to perform Gaussian elimination on a given matrix. It includes the following functions:

- `gaussian_elimination(matrix)`: Performs Gaussian elimination on the input matrix and returns the row-echelon form of the matrix.

### matrix_operation.py

This script contains various matrix operations, including:

- `add_matrices(matrix1, matrix2)`: Adds two matrices.
- `subtract_matrices(matrix1, matrix2)`: Subtracts the second matrix from the first matrix.
- `multiply_matrices(matrix1, matrix2)`: Multiplies two matrices.
- `invert_matrix(matrix)`: Inverts the given matrix (if possible).

### Makefile

The Makefile includes targets to build and run the project. The main targets are:

- `all`: Builds the project by running the Python scripts.
- `clean`: Cleans up any generated files.

To build and run the project using the Makefile, simply run `make` in the project directory.

## Example

Here is an example of how to use the scripts in this project:

### Gaussian Elimination

```python
from gauss import gaussian_elimination

matrix = [
    [2, 1, -1, 8],
    [-3, -1, 2, -11],
    [-2, 1, 2, -3]
]

result = gaussian_elimination(matrix)
print("Row-Echelon form of the matrix:")
for row in result:
    print(row)
```

### Matrix Operations

```python
from matrix_operation import add_matrices, subtract_matrices, multiply_matrices, invert_matrix

matrix1 = [
    [1, 2],
    [3, 4]
]

matrix2 = [
    [5, 6],
    [7, 8]
]

print("Matrix Addition:")
print(add_matrices(matrix1, matrix2))

print("Matrix Subtraction:")
print(subtract_matrices(matrix1, matrix2))

print("Matrix Multiplication:")
print(multiply_matrices(matrix1, matrix2))

print("Matrix Inversion:")
print(invert_matrix(matrix1))
```

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request.
