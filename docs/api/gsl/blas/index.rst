:mod:`gsl.blas`
===============

.. py:module:: gsl.blas

.. autoapi-nested-parse::

   Support for the BLAS interface



Module Contents
---------------

.. function:: ddot(x, y)

   Compute the scalar product {x^T y}


.. function:: dnrm2(x)

   Compute the Euclidean norm


.. function:: dasum(x)

   Compute the sum of the absolute values of the entries in {x}


.. function:: idamax(x)

   Return the index with the largest value in {x}


.. function:: dswap(x, y)

   Exchange the contents of {x} and {y}


.. function:: dcopy(x, y)

   Copy the elements of {x} into {y}


.. function:: daxpy(α, x, y)

   Compute {α x + y} and store the result in {y}


.. function:: dscal(α, x)

   Compute x = α x


.. function:: drotg(x, y)

   Compute the Givens rotation which zeroes the vectors {x} and {y}


.. function:: drot(x, y, c, s)

   Apply the Givens rotation {(c,s)} to {x} and {y}


.. function:: dgemv(transpose, α, A, x, β, y)

   Compute {y = α op(A) x + β y}


.. function:: dtrmv(uplo, transpose, diag, A, x)

   Compute {x = op(A) x}


.. function:: dtrsv(uplo, transpose, diag, A, x)

   Compute {x = inv(op(A)) x}


.. function:: dsymv(uplo, α, A, x, β, y)

   Compute {y = α A x + β y}


.. function:: dsyr(uplo, α, x, A)

   Compute {A = α x x^T + A}


.. function:: dgemm(tranA, tranB, α, A, B, β, C)

   Compute {C = α op(A) op(B) + β C}


.. function:: dsymm(side, uploA, α, A, B, β, C)

   Compute {C = α A B + β C} or {C = α B A + β C} depending on {side}, A is symmetric


.. function:: dtrmm(sideA, uplo, transpose, diag, α, A, B)

   Compute {B = α op(A) B} or {B = α B op(A)} depending on the value of {sideA}


