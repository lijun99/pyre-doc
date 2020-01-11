:mod:`cuda`
===========

.. py:module:: cuda


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Device/index.rst
   DeviceManager/index.rst
   Matrix/index.rst
   Stats/index.rst
   Timer/index.rst
   Vector/index.rst
   cuBlas/index.rst
   cuRand/index.rst
   cuSolverDn/index.rst
   exceptions/index.rst


Package Contents
----------------

.. data:: msg
   :annotation: = could not find 'cuda' support

   

.. data:: version
   

   

.. data:: copyright
   

   

.. function:: license()


.. py:class:: DeviceManager(**kwds)

   The singleton that provides access to what is known about CUDA capable hardware

   .. attribute:: count
      :annotation: = 0

      

   .. attribute:: devices
      :annotation: = []

      

   .. attribute:: current_device
      

      

   .. method:: device(self, did=0)


      Set {did} as the default device



.. data:: manager
   

   

.. data:: devices
   

   

.. data:: device
   

   

.. py:class:: vector(shape=1, source=None, dtype='float64', **kwds)

   cuda vector (a python wrapper for c/c++ cuda_vector)
   typedef struct {
       size_t size; // length
       char *data; // pointer to gpu memory
       size_t nbytes; // total bytes
       int dtype; // use numpy type_num
   } cuda_vector;

   .. attribute:: data
      

      

   .. method:: copy_to_host(self, target=None, type='gsl')


      copy cuda vector to host (gsl or numpy)vector
      gsl.vector is double precison only
      numpy.ndarray can be any type


   .. method:: copy_from_host(self, source)


      copy from a host (gsl or numpy) vector


   .. method:: copy(self, other)


      copy data from another vector


   .. method:: clone(self)


      clone to a new vector


   .. method:: zero(self)


      initialize all elements to 0


   .. method:: fill(self, value)


      set all elements to a given value


   .. method:: print(self)


      print elements by converting to numpy ndarray


   .. method:: sum(self)


      summation


   .. method:: amin(self)


      minimum value


   .. method:: amax(self)


      maximum value


   .. method:: mean(self)


      mean value


   .. method:: std(self, mean=None, ddof=1)


      standard deviation
      :param mean: mean value
      :param ddof: delta degrees of freedom, or the dividing factor(n-ddof)


   .. method:: free(self)


      force releasing gpu memory
      :return:


   .. method:: bcast(self, communicator=None, source=0)


      Broadcast the given {vector} from {source} to all tasks in {communicator}


   .. method:: size(self)
      :property:



   .. method:: __len__(self)



   .. method:: __iadd__(self, other)


      In-place addition with the elements of {other}


   .. method:: __isub__(self, other)


      In-place subtraction with the elements of {other}


   .. method:: __imul__(self, other)


      In-place scale with a factor {other}


   .. method:: __getitem__(self, index)


      Get the value of v[index]
      :param index: index of the vector
      :return: float value (in cpu)



.. py:class:: matrix(shape=(1, 1), source=None, dtype='float64', **kwds)

   cuda matrix ( a python wrapper for c/c++ cuda_matrix )

   typedef struct {
       size_t size1; // shape[0]
       size_t size2; // shape[1]
       size_t size;  // total size
       char *data; // pointer to gpu memory
       size_t nbytes; // total bytes
       int dtype; // use numpy type_num
   } cuda_matrix;

   properties:
       shape[2]: shape (size1, size2)
       data: PyCapsule for c/c++ cuda_matrix object
       dtype: data type as in numpy
       size: shape[0]*shape[1]

   .. attribute:: submatrix
      

      

   .. attribute:: data
      

      

   .. method:: copy_to_host(self, target=None, type='gsl')


      copy cuda matrix to host (gsl or numpy)
      gsl.matrix is double precison only
      numpy.ndarray can be any type


   .. method:: copy_from_host(self, source)


      copy from a gsl(host) matrix


   .. method:: copy(self, other)


      copy data from another matrix


   .. method:: copy_to_device(self, out=None, dtype=None)


      Copy a matrix to another gpu matrix with type conversion support
      :param out: pre-allocated output matrix
      :param dtype: output matrix data type if out is none
      :return: out


   .. method:: clone(self)


      clone to a new matrix


   .. method:: view(self, out=None, start=(0, 0), size=None)


      copy a submatrix with size=(m,n) from start=(ms, ns)


   .. method:: tovector(self, start=(0, 0), size=None, out=None)


      view a continuous part or whole matrix as a vector (without data copying)
      :param start: tuple (row, col) as starting element
      :param size: number of elements in vector
      :return: a cuda vector of size size


   .. method:: get_row(self, row=0, out=None)


      get one row
      :param row: row index
      :return: a cuda vector of size=columns


   .. method:: set_row(self, src, row=0)


      set one row from a vector
      :param src: cuda vector
      :param row: row index
      :return: self


   .. method:: insert(self, src, start=(0, 0), shape=None)


      insert (copy) a matrix from position start


   .. method:: copytile(self, src, start=(0, 0), src_start=(0, 0), shape=None)


      copy a tile of matrix from src


   .. method:: copycols(self, dst, indices, batch=None)


      copy one or more columns to another matrix, the columns to be copied are specified by indices
      :param dst:
      :param indices:
      :param batch:
      :return:


   .. method:: duplicateVector(self, src, size=None, incx=1)


      Copy a vector to first one or few rows to this matrix
      :param src:  cuda vector
      :param size:
      :param incx:
      :return:


   .. method:: copy_triangle(self, fill=1)


      for nxn triangular matrix, copy upper triangle (fill=1) to lower, or vice versa(fill=0)
      :param fill: 0,1 for lower/upper filled matrix
      :return: self


   .. method:: zero(self)


      initialize all elements to 0


   .. method:: fill(self, value)


      set all elements to a given value


   .. method:: print(self)


      print elements by converting to gsl(host) matrix at first


   .. method:: transpose(self, out=None)


      transpose M(m,n)-> MT(n,m)


   .. method:: inverse_cholesky(self, out=None, uplo=1)


      Matrix inverse (in place if out is not provided) for symmetric matrix only
      only the lower, upper part is used for uplo=0,1


   .. method:: inverse(self, out=None)


      Matrix inverse with LU
      :param out: output matrix if different from input
      :param uplo: inverse matrix store mode
      :return: self or out


   .. method:: Cholesky(self, out=None, uplo=1)


      Cholesky decomposition
      :param out: output matrix
      :param uplo: store mode for output, 0/1 = lower/upper triangle
      :return: self or out


   .. method:: determinant(self, triangular=False)


      matrix determinant for real symmetric matrix


   .. method:: log_det(self, triangular=False)


      matrix log determinant for real symmetric matrix


   .. method:: amin(self)


      minimum value


   .. method:: amax(self)


      maximum value


   .. method:: mean(self, axis=None, out=None)


      mean values along axis=0(row), 1(column), or all elements (None)
      :param axis: int or None, axis along which the means are computed. None for all elements
      :param out: output vector for axis=0,1  vector size = columns(axis=0), rows(axis=1)
      :return:  mean value(s) as a vector for axis=0 or 1, as a float


   .. method:: mean_sd(self, axis=0, out=None, ddof=1)


      mean and stand deviations along row or column
      :param axis: int or None, axis along which the means are computed. None for all elements
      :param out: tuple of two vectors (mean, sd), vector size is 1 (axis=None),  columns(axis=0), rows(axis=1)
      :param ddof: delta degrees of freedom
      :return: tuple of two vectors


   .. method:: free(self)


      force releasing gpu memory
      :return:


   .. method:: bcast(self, communicator=None, source=0)


      Broadcast the given {vector} from {source} to all tasks in {communicator}


   .. method:: rows(self)
      :property:



   .. method:: cols(self)
      :property:



   .. method:: __iadd__(self, other)


      In-place addition with the elements of {other}


   .. method:: __isub__(self, other)


      In-place subtraction with the elements of {other}


   .. method:: __imul__(self, other)


      In-place scale with a factor {other}



.. py:class:: curand

   CURAND lib utitilies

   .. attribute:: CURAND_RNG_TEST
      :annotation: = [0]

      

   .. attribute:: CURAND_RNG_PSEUDO_DEFAULT
      :annotation: = 100

      

   .. attribute:: CURAND_RNG_PSEUDO_XORWOW
      :annotation: = 101

      

   .. attribute:: CURAND_RNG_PSEUDO_MRG32K3A
      :annotation: = 121

      

   .. attribute:: CURAND_RNG_PSEUDO_MTGP32
      :annotation: = 141

      

   .. attribute:: CURAND_RNG_PSEUDO_MT19937
      :annotation: = 142

      

   .. attribute:: CURAND_RNG_PSEUDO_PHILOX4_32_10
      :annotation: = 161

      

   .. attribute:: CURAND_RNG_QUASI_DEFAULT
      :annotation: = 200

      

   .. attribute:: CURAND_RNG_QUASI_SOBOL32
      :annotation: = 201

      

   .. attribute:: CURAND_RNG_QUASI_SCRAMBLED_SOBOL32
      :annotation: = 202

      

   .. attribute:: CURAND_RNG_QUASI_SOBOL64
      :annotation: = 203

      

   .. attribute:: CURAND_RNG_QUASI_SCRAMBLED_SOBOL64
      :annotation: = 204

      

   .. method:: create_generator(gentype=None, seed=None)


      allocate a curand generator 


   .. method:: set_seed(gen, seed)


      Set seed for curand generator


   .. method:: get_current_generator()


      Find the curand generator from current device


   .. method:: gaussian(gen=None, out=None, dtype='float64', loc=0, scale=1, size=1)


      generate Gaussian(Normal) distribution random numbers 


   .. method:: uniform(gen=None, out=None, dtype='float64', size=1)


      generate uniform distribution random numbers (0,1] 



.. py:class:: cublas

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



.. py:class:: cusolverdn

   Wrapper for cusolverDn lib utitilies

   .. method:: create_handle()


      create a cusolverDn handle


   .. method:: get_current_handle()




.. py:class:: timer(**kwds)

   A cuda timer using cudaEvent

   .. attribute:: capsule
      

      

   .. method:: start(self)



   .. method:: stop(self)



   .. method:: profile(self, process, *args, **kwargs)


      Profile a process
      :param process:
      :param args:
      :return:



.. function:: current_device()

   return current device


