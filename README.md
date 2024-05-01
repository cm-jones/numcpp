# lincpp: Numerical Linear Algebra for C++

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

LinCPP is an open-source, numerical linear algebra library for C++ that implements common operations on vectors and matrices as well as important algorithms in linear algebra.

## Features

- For a square matrix $A$, computing:
  - $tr(A)$, the trace of A
  - $det(A)$, the determinate of A
  - $A^T$, the transpose of A
  - $A^{-1}$, the inverse of A (if and only if $det(A) = 0$)
  - $A^n$, the integer powers of A
- For any matrix $A$, computing:
  - the LU, QR, and SVD factorizations of $A$
  - solving a system of linear equations ($Ax = b$)
  - the eigenvalues ($\lambda$) and eigenvectors ($x$) of $A$ ($Ax = \lambda x$)

## Installation

### Requirements

- C++14 or later
- CMake 3.10 or later

### Build and Install

1. Clone the repository:
   ```
   git clone https://github.com/cm-jones/lincpp.git
   ```

2. Create a build directory and navigate to it:
   ```
   cd lincpp
   mkdir build
   cd build
   ```

3. Run CMake to configure the project:
   ```
   cmake ..
   ```

4. Build the library:
   ```
   make
   ```

5. (Optional) Install the library and headers:
   ```
   sudo make install
   ```

## Usage

Include the necessary headers in your C++ source files:

```cpp
#include <numcpp/vector.h>
#include <numcpp/matrix.h>
```

Create vectors and matrices, and perform operations on them:

```cpp
using namespace lincpp;

Matrix<double> A(2, 2);
A(0, 0) = 1.0;
A(0, 1) = 2.0;
A(1, 0) = 3.0;
A(1, 1) = 4.0;

Vector<double> b(2);
b(0) = 5.0;
b(1) = 6.0;

Vector<double> x = solve(A, b);
```

## Documentation

Detailed documentation for LinCPP can be found under [docs/](docs/).

## Contributing

If you find any issues or have suggestions for improvements, feel free to [open an issue](https://github.com/cm-jones/lincpp/issues/new) or submit a [pull request](https://github.com/cm-jones/lincpp/compare).

## License

This project is licensed under the [GNU General Public License v3.0](LICENSE).
