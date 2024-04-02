# Iterative-Linear-Solver-for-Sparse-System

## Introduction
There are 3 most common linear iterative solvers for solving Sparse Linear Systems: Jacobi、Gauss-Seidel and Preconditioned-Conjugate-Gradient.

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

Jacobi

<p><strong>&bull;</strong> comparison of serial and parallel speed <p>

<p><strong>&bull;</strong> effects of Chebyshev acceleration <p>

## Gauss-Seidel
<p><strong>&bull;</strong> simulation effects <p>

<p><strong>&bull;</strong> comparison of serial and parallel speed <p>

## PCG
<p><strong>&bull;</strong> simulation effects <p>

<p><strong>&bull;</strong> comparison of different preconditioners <p>

## Future Work
<p><strong>&bull;</strong> continue to improve the overall performance of the code <p> 
