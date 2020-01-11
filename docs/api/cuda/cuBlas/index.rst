:mod:`cuda.cuBlas`
==================

.. py:module:: cuda.cuBlas


Module Contents
---------------

.. py:class:: cuBlas

   Wrapper for cublas lib utitilies

   .. attribute:: CUBLAS_FILL_MODE_LOWER
      :annotation: = 0

      

   .. attribute:: CUBLAS_FILL_MODE_UPPER
      :annotation: = 1

      

   .. attribute:: CUBLAS_FILL_MODE_FULL
      :annotation: = 2

      

   .. attribute:: CUBLAS_DIAG_NON_UNIT
      :annotation: = 0

      

   .. attribute:: CUBLAS_DIAG_UNIT
      :annotation: = 1

      

   .. attribute:: CUBLAS_SIDE_LEFT
      :annotation: = 0

      

   .. attribute:: CUBLAS_SIDE_RIGHT
      :annotation: = 1

      

   .. attribute:: CUBLAS_OP_N
      :annotation: = 0

      

   .. attribute:: CUBLAS_OP_T
      :annotation: = 1

      

   .. attribute:: CUBLAS_OP_C
      :annotation: = 2

      

   .. attribute:: CUBLAS_OP_HERMITAN
      :annotation: = 2

      

   .. attribute:: CUBLAS_OP_CONJG
      :annotation: = 3

      

   .. attribute:: FillModeLower
      :annotation: = 0

      

   .. attribute:: FillModeUpper
      :annotation: = 1

      

   .. attribute:: DiagNonUnit
      :annotation: = 0

      

   .. attribute:: DiagUnit
      :annotation: = 1

      

   .. attribute:: SideLeft
      :annotation: = 0

      

   .. attribute:: SideRight
      :annotation: = 1

      

   .. attribute:: OpNoTrans
      :annotation: = 0

      

   .. attribute:: OpTrans
      :annotation: = 1

      

   .. method:: create_handle()


      create a cublas handle


   .. method:: get_current_handle()



   .. method:: axpy(alpha, x, y, handle=None, batch=None, incx=1, incy=1)


      axpy : y = alpha x + y


   .. method:: gemm(A, B, handle=None, out=None, alpha=1.0, beta=0.0, rows=None, transa=0, transb=0)


      Matrix-matrix multiplication (no complex support yet)
      Args: op(A) with shape(m,k), op(B) with shape (k, n) in row major
            op(A) = A if transa=0, else A^T
            rows - only first rows are calculated (rows <=m)
      Returns: out (C) with shape (m, n)
              C = alpha A B + beta C


   .. method:: gemv(A, x, handle=None, out=None, trans=0, alpha=1.0, beta=0.0)


      y(out) = alpha op(A) x + beta y
      :param A: matrix (m, n)
      :param x: vector with size= n/m if trans=0/1 (notrans/transpose)
      :param handle: cublas handle
      :param out: vector y with size = m/n if trans=0/1
      :param trans:
      :param alpha:
      :param beta:
      :return: y


   .. method:: trmv(A, x, handle=None, uplo=1, transa=0, diag=0, incx=1, n=None)


      triangular matrix-vector multiplication x= op(A) x
      Args: A symmetric nxn, x vector n
      Return: x


   .. method:: trmm(A, B, handle=None, out=None, alpha=1.0, uplo=1, side=0, transa=0, diag=0)


      symmetric matrix-matrix multiplication C= A B (Note in blas B = A B)
      Args: if SideLeft A symmetric mxm, B mxn
            if SideRight, A symmetric nxn B mxn
      Return: out(C)  m x n


   .. method:: symv(A, x, handle=None, uplo=1, n=None, alpha=1.0, beta=0.0, out=None)


      symmetric matrix-vector multiplication y = alpha A x + beta y
      Args: A symmetric nxn, x vector n
      Return: x


   .. method:: symm(A, B, handle=None, out=None, alpha=1.0, beta=0.0, uplo=1, side=0)


      symmetric matrix-matrix multiplication C= A B (Note in blas B = A B)
      Args: if SideLeft A symmetric mxm, B mxn
            if SideRight, A symmetric nxn B mxn
      Return: out(C)  m x n



