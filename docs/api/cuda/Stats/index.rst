:mod:`cuda.Stats`
=================

.. py:module:: cuda.Stats


Module Contents
---------------

.. py:class:: Stats

   Statistics Routines for cuda vectors ana matrices

   .. method:: amin(a)


      Return the minimum of a vector or a matrix or minimum along an axis.
      :param a: a cuda vector or matrix
      :return: the minimum value


   .. method:: amax(a)


      Return the maximum of a vector or a matrix or maximum along an axis.
      :param a: a cuda vector or matrix
      :return: the maximum value


   .. method:: l1norm(x, size=None, stride=1)


      L1 norm of a vector \sum_i |x_i|
      :return:


   .. method:: l2norm(x, size=None, stride=1)


      L2 norm of a vector \sqrt{\sum_i x_i^2}
      :return:


   .. method:: linfnorm(x, size=None, stride=1)


      L-Infinity norm of a vector max|x_i|
      :return:


   .. method:: covariance(x, y, out=None, axis=0, ddof=1)


      Compute covariance between two vectors or matrices (along row or col)
      cov(X,Y) = E[(X-E[X])(Y-E[Y])]
      :param x, y: two input vectors or matrices
      :param axis: (for matrices only) 0/1 = along row/col
      :param out: (for matrices only) vector of size shape[1]/shape[0] for axis = 0/1
      :return: float for vectors, vector for matrices


   .. method:: correlation(x, y, axis=0, out=None)


      Compute correlation between two vectors or matrices (along row or col)
      cor(X,Y) = cov(X, Y)/ (std(X)std(Y))
      :param y:
      :param axis:
      :param out:
      :return:


   .. method:: max_diff(x, y)


      compute maximum difference between elements of two vectors or matrices
      max{|x_i - y_i|}
      :param x, y: two vectors or matrices
      :return: the maximum difference max|x_i - y_i|



