Jacobi Method: Serial and Parallel Implementations
==================================================

This repository contains implementations of the Jacobi iterative method in Python and C++, designed for solving systems of linear equations efficiently. The project demonstrates both serial and parallel approaches, with a strong emphasis on performance benchmarking using parallelism and multithreading.

Features
--------

*   **Matrix and Vector Initialization**: Automatically generate a diagonally dominant matrix and a corresponding vector.
    
*   **Serial Implementation**: A basic version of the Jacobi method, executed sequentially.
    
*   **Parallel Implementation**: A multithreaded version that leverages multiprocessing in Python and C++'s threading capabilities.
    
*   **Performance Benchmarking**: Includes options for running strong scaling tests to evaluate speedups with different thread counts.
    

Requirements
------------

### Python

*   Python 3.8 or higher
    
*   Required libraries: numpy, argparse, multiprocessing
    

### C++

*   C++17 or later
    
*   Compiler supporting threading (e.g., g++, clang)
    

How to Run
----------

### Python Implementation
```bash
  python main.py -n <number of n> -t <number of threads>
``` 

#### Arguments:

*   \-n: Size of the matrix (required, e.g., -n 100)
    
*   \-t: Number of threads for the parallel implementation (default: 1)
    
*   \--test-scaling: Run strong scaling tests with multiple thread counts (1, 2, 4, 8).
    

#### Examples:

```bash
python main.py -n 100 -t 4
```

    
```bash
python main.py -n 100 --test-scaling
```
    
----------
### C++ Implementation

```bash
eg++ jacobi_parallel.cpp -o jacobi\_parallel -std=c++17 -pthread

```
```bash
./jacobi_parallel -n <number of n> -t <number of threads>
```    

#### Arguments:

*   \-n: Size of the matrix (required, e.g., -n 100)
    
*   \-t: Number of threads for the parallel implementation (default: 1)
    
*   \--test-scaling: Run strong scaling tests with multiple thread counts (1, 2, 4, 8).
    

#### Examples:

```bash
./jacobi_parallel -n 100 -t 4

```
    
```bash
./jacobi_parallel -n 100 --test-scaling
```
    

### Strong Scaling Test

The --test-scaling flag evaluates the performance of the parallel Jacobi method by testing execution times across multiple thread counts (1, 2, 4, 8). The results showcase how increasing the number of threads improves computational speed while revealing the limitations of parallel efficiency.


Key Learning Points
-------------------

*   Understanding the Jacobi method for solving linear equations.
    
*   Exploring the benefits and limitations of parallel computing.
    
*   Comparing the performance of Python and C++ implementations.
    

License
-------

This project is licensed under the Apache License
