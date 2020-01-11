:mod:`gsl.linalg`
=================

.. py:module:: gsl.linalg

.. autoapi-nested-parse::

   Support for the linear algebra interface



Module Contents
---------------

.. function:: LU_decomposition(matrix)

   Compute the LU decomposition of a matrix


.. function:: LU_invert(matrix, permutation, sign)

   Compute the inverse of {matrix} given its LU decomposition; a new matrix is returned


.. function:: LU_det(matrix, permutation, sign)

   Compute the determinant of {matrix} given its LU decomposition


.. function:: LU_lndet(matrix, permutation, sign)

   Compute the determinant of {matrix} given its LU decomposition


.. function:: cholesky_decomposition(matrix)

   Compute the Cholesky decomposition of a symmetric positive definite matrix


