:mod:`gsl.Matrix`
=================

.. py:module:: gsl.Matrix


Module Contents
---------------

.. py:class:: Matrix(shape, data=None, **kwds)

   A wrapper over a gsl matrix

   .. attribute:: defaultFormat
      :annotation: = +16.7

      

   .. attribute:: upperTriangular
      :annotation: = 1

      

   .. attribute:: lowerTriangular
      :annotation: = 0

      

   .. attribute:: unitDiagonal
      :annotation: = 1

      

   .. attribute:: nonUnitDiagonal
      :annotation: = 0

      

   .. attribute:: opNoTrans
      :annotation: = 0

      

   .. attribute:: opTrans
      :annotation: = 1

      

   .. attribute:: opConjTrans
      :annotation: = 2

      

   .. attribute:: sideRight
      :annotation: = 1

      

   .. attribute:: sideLeft
      :annotation: = 0

      

   .. attribute:: sortValueAscending
      :annotation: = 0

      

   .. attribute:: sortValueDescending
      :annotation: = 1

      

   .. attribute:: sortMagnitudeAscending
      :annotation: = 2

      

   .. attribute:: sortMagnitudeDescending
      :annotation: = 3

      

   .. attribute:: data
      

      

   .. attribute:: shape
      :annotation: = [0, 0]

      

   .. method:: bcast(cls, matrix=None, communicator=None, source=0)
      :classmethod:


      Broadcast the given {matrix} from {source} to all tasks in {communicator}


   .. method:: collect(cls, matrix, communicator=None, destination=0)
      :classmethod:


      Gather the data in {matrix} from each task in {communicator} into one big matrix
      available at the {destination} task


   .. method:: excerpt(self, communicator=None, source=0, matrix=None)


      Scatter {matrix} held by the task {source} among all tasks in {communicator} and fill me
      with the partition values. Only {source} has to provide a {matrix}; the other tasks can
      use the default value.


   .. method:: columns(self)
      :property:


      Get the number of columns


   .. method:: rows(self)
      :property:


      Get the number of rows


   .. method:: elements(self)
      :property:


      Iterate over all my elements


   .. method:: zero(self)


      Set all my elements to zero


   .. method:: fill(self, value)


      Set all my elements to {value}


   .. method:: view(self, start, shape)


      Build a view to my data anchored at {start} with the given {shape}


   .. method:: load(self, filename, binary=None)


      Read my values from {filename}

      This method attempts to distinguish between text and binary representations of the
      data, based on the parameter {mode}, or the {filename} extension if {mode} is absent


   .. method:: save(self, filename, binary=None, format=defaultFormat)


      Write my values to {filename}

      This method attempts to distinguish between text and binary representations of the
      data, based on the parameter {mode}, or the {filename} extension if {mode} is absent


   .. method:: read(self, filename)


      Read my values from {filename}


   .. method:: write(self, filename)


      Write my values to {filename}


   .. method:: scanf(self, filename)


      Read my values from {filename}


   .. method:: printf(self, filename, format=defaultFormat)


      Write my values to {filename}


   .. method:: print(self, format='{:+13.4e}', indent='', interactive=True)


      Print my values using the given {format}


   .. method:: identity(self)


      Initialize me as an identity matrix: all elements are set to zero except along the
      diagonal, which are set to one


   .. method:: random(self, pdf)


      Fill me with random numbers using the probability distribution {pdf}


   .. method:: clone(self)


      Allocate a new matrix and initialize it using my values


   .. method:: copy(self, other)


      Fill me with values from {other}, which is assumed to be of compatible shape


   .. method:: tuple(self)


      Build a representation of my contents as a tuple of tuples

      This is suitable for converting to other matrix representations, such as numpy


   .. method:: transpose(self, destination=None)


      Compute the transpose of a matrix.

      If {destination} is {None} and the matrix is square, the operation happens
      in-place. Otherwise, the transpose is stored in {destination}, which is assumed to be
      shaped correctly.


   .. method:: getRow(self, index)


      Return a view to the requested row


   .. method:: getColumn(self, index)


      Return a view to the requested column


   .. method:: setRow(self, index, v)


      Set the row at {index} to the contents of the given vector {v}


   .. method:: setColumn(self, index, v)


      Set the column at {index} to the contents of the given vector {v}


   .. method:: max(self)


      Compute my maximum value


   .. method:: min(self)


      Compute my maximum value


   .. method:: minmax(self)


      Compute my minimum and maximum values


   .. method:: symmetricEigensystem(self, order=sortValueAscending)


      Computed my eigenvalues and eigenvectors assuming i am a real symmetric matrix


   .. method:: mean(self, axis=None, out=None)


      Compute the mean values of a matrix
      axis = None, 0, or 1, along which the mean are computed


   .. method:: mean_sd(self, axis=None, out=None, sample=True)


      Compute the mean values of matrix
      axis: int or None
           axis along which the means are computed. None for all elements
      out: tuple of two vectors (mean, sd)
           vector size is 1 (axis=None),  columns(axis=0), rows(axis=1)
      sample: True or False
           when True, the sample standard deviation is computed 1/(N-1)
           when False, the population standard deviation is computed 1/N


   .. method:: std(self, axis=None, sample=False)


      Compute the standard deviation of a matrix


   .. method:: ndarray(self, copy=False)


      Return a numpy array reference (w/ shared data) if {copy} is False, or a new copy if {copy} is {True}


   .. method:: __iter__(self)


      Iterate over all my elements in shape order


   .. method:: __contains__(self, value)



   .. method:: __getitem__(self, index)



   .. method:: __setitem__(self, index, value)



   .. method:: __eq__(self, other)



   .. method:: __ne__(self, other)



   .. method:: __iadd__(self, other)


      In-place addition with the elements of {other}


   .. method:: __isub__(self, other)


      In-place subtraction with the elements of {other}


   .. method:: __imul__(self, other)


      In-place multiplication with the elements of {other}


   .. method:: __itruediv__(self, other)


      In-place addition with the elements of {other}



