# Iterative-Solver-for-Sparse-System

## Introduction
There are 3 most common linear iterative solvers for solving Sparse Linear Systems: Jacobi、Gauss-Seidel and Preconditioned-Conjugate-Gradient.
The test scene is of an armadillo whose ears and hands are fixed and deformed by gravity.

## Features
<p><strong>&bull;</strong> serial and parallel implementations of Jacobi solver with Chebyshev acceleration <p> 
  
<p><strong>&bull;</strong> serial and parallel implemantations of Gauss-Seidel solver <p>
  
<p><strong>&bull;</strong> the convergence of both Jacobi and GS solver can be controled by adjusting the relaxation <p>
  
<p><strong>&bull;</strong> the parallel version of Gauss-Seidel is based on random graph coloring algorithm <p>
  
<p><strong>&bull;</strong> the implementation of the preconditioner contains Jacobi、incomplete-Cholesky factorization and SSOR <p>

the parallel implementation is based on [oneTBB](https://github.com/oneapi-src/oneTBB)

and the relevant linear algebra operations are based on [Eigen](https://eigen.tuxfamily.org/dox/group__TutorialSparse.html)

## Results

<p><strong>&bull;</strong> simulation effects <p>

![arma_gra](results/arma_gra.gif)

### PCG 

compared the effects of different preconditioners on CG convergence: 

<p><strong>&bull;</strong> Jacobi Preconditioner: 18 iterations <p>
  
<p><strong>&bull;</strong> incomplete Cholesky Preconditioner: 5 iterations <p>
  
<p><strong>&bull;</strong> SSOR Preconditioner: 8 iterations <p>  

### Gauss-Seidel

compared the serial and parallel speed with relaxation = 1

<p><strong>&bull;</strong> time of solving system in parallel = 1.1 ms <p> 

<p><strong>&bull;</strong> time of serial solving system = 3.5 ms <p>

### Jacobi

compared the serial and parallel speed with relaxation = 0.3

<p><strong>&bull;</strong> time of solving system in parallel = 8 ms <p> 

<p><strong>&bull;</strong> time of solving system in serial = 50 ms <p> 

compared the effects of chebyshev acceleration 

<p><strong>&bull;</strong> with chebyshev acceleration: 17 iterations <p> 

<p><strong>&bull;</strong> without chebyshev acceleration: 45 iterations <p> 

## Future Work
<p><strong>&bull;</strong> construct graphs in parallel to improve the performence of graph generation <p> 
