:mod:`cuda.Matrix`
==================

.. py:module:: cuda.Matrix


Module Contents
---------------

.. py:class:: Matrix(shape=(1, 1), source=None, dtype='float64', **kwds)

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



