:mod:`gsl`
==========

.. py:module:: gsl


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Histogram/index.rst
   Matrix/index.rst
   MatrixView/index.rst
   Permutation/index.rst
   RNG/index.rst
   Vector/index.rst
   VectorView/index.rst
   blas/index.rst
   exceptions/index.rst
   linalg/index.rst
   pdf/index.rst
   stats/index.rst


Package Contents
----------------

.. function:: zero(entity)

   Zero out the content of {entity}


.. function:: fill(entity, value)

   Set all entries in {entity} to {value}


.. data:: msg
   :annotation: = could not load the 'gsl' extension module

   

.. data:: package
   

   

.. data:: version
   

   

.. data:: copyright
   

   

.. function:: license()


.. py:class:: histogram(bins, data=None, **kwds)

   A wrapper over a gsl histogram

   .. attribute:: bins
      :annotation: = 0

      

   .. attribute:: data
      

      

   .. method:: uniform(self, lower, upper)


      Adjust the histogram bins to cover the range [lower, upper) uniformly. The values of
      the bins are reset to zero


   .. method:: ranges(self, points)


      Use {points} to define the histogram bins. {points} is expected to be an iterable of
      size one greater than the size of the histogram itself; the extra element is used to
      specify the upper value of the last bin. The entries in {points} must be monotonically
      increasing


   .. method:: reset(self)


      Reset the values of all the bins to zero


   .. method:: increment(self, x)


      Increment by one the bin whose range contains {x}


   .. method:: accumulate(self, x, weight)


      Add {weight} to the bin whose range contains {x}


   .. method:: fill(self, values)


      Increment my frequency counts using the contents of the vector {values}


   .. method:: clone(self)


      Allocate a new histogram and initialize it using my values


   .. method:: copy(self, other)


      Make me an exact copy of {other}


   .. method:: values(self)


      Return a vector that contains the values from each of my bins. This is equivalent to

      v = gsl.vector.alloc(shape=self.bins)
      for i in range(self.bins):
          v[i] = self[i]
      return v


   .. method:: find(self, x)


      Return the index of the bin that contains the value {x}


   .. method:: max(self)


      Return my maximum upper range


   .. method:: min(self)


      Return my minimum lower range


   .. method:: range(self, i)


      Return a tuple [lower, upper) that describes the range of the {i}th bin


   .. method:: max_bin(self)


      Return the index of the bin where maximum value is contained in the histogram


   .. method:: max_value(self)


      Return the maximum value contained in the histogram


   .. method:: min_bin(self)


      Return the index of the bin where minimum value is contained in the histogram


   .. method:: min_value(self)


      Return the minimum value contained in the histogram


   .. method:: mean(self)


      Return the mean of the histogrammed variable


   .. method:: sdev(self)


      Return the standard deviation of the histogrammed variable


   .. method:: sum(self)


      Return the sum of all bin values


   .. method:: __len__(self)



   .. method:: __iter__(self)



   .. method:: __getitem__(self, index)



   .. method:: __iadd__(self, other)


      In-place addition with the elements of {other}


   .. method:: __isub__(self, other)


      In-place subtraction with the elements of {other}


   .. method:: __imul__(self, other)


      In-place multiplication with the elements of {other}


   .. method:: __itruediv__(self, other)


      In-place addition with the elements of {other}



.. py:class:: matrix(shape, data=None, **kwds)

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



.. py:class:: permutation(shape, data=None, **kwds)

   A wrapper over a gsl permutation

   .. attribute:: data
      

      

   .. attribute:: shape
      

      

   .. method:: init(self)


      Initialize a permutation


   .. method:: clone(self)


      Allocate a new permutation and initialize it using my values


   .. method:: reverse(self)


      Reverse me


   .. method:: inverse(self)


      Reverse me


   .. method:: swap(self, other)


      Swap me with {other}


   .. method:: size(self)


      Compute my size


   .. method:: next(self)


      Compute the next permutation in my sequence


   .. method:: prev(self)


      Compute the prev permutation in my sequence


   .. method:: __bool__(self)



   .. method:: __len__(self)



   .. method:: __iter__(self)



   .. method:: __getitem__(self, index)




.. py:class:: rng(algorithm='ranlxs2', **kwds)

   Encapsulation of the pseudo-random number generators in GSL

   .. attribute:: available
      

      

   .. attribute:: rng
      

      

   .. method:: algorithm(self)
      :property:



   .. method:: range(self)
      :property:



   .. method:: float(self)


      Return a random float in the range [0, 1)


   .. method:: int(self)


      Return a random integer within the range of the generator


   .. method:: seed(self, seed=0)


      Initialize the RNG with the given seed



.. py:class:: vector(shape, data=None, **kwds)

   A wrapper over a gsl vector

   .. attribute:: defaultFormat
      :annotation: = +16.7

      

   .. attribute:: data
      

      

   .. method:: bcast(cls, vector=None, communicator=None, source=0)
      :classmethod:


      Broadcast the given {vector} from {source} to all tasks in {communicator}


   .. method:: collect(cls, vector, communicator=None, destination=0)
      :classmethod:


      Gather the data in {vector} from each task in {communicator} into one big vector
      available at the {destination} task


   .. method:: excerpt(self, communicator=None, source=0, vector=None)


      Scatter {vector} held by the task {source} among all tasks in {communicator} and fill me
      with the partition values. Only {source} has to provide a {vector}; the other tasks can
      use the default value.


   .. method:: elements(self)
      :property:


      Iterate over all my elements


   .. method:: zero(self)


      Set all my elements to zero


   .. method:: fill(self, value)


      Set all my elements to {value}


   .. method:: basis(self, index)


      Initialize me as a basis vector: all elements are set to zero except {index}, which is
      set to one


   .. method:: random(self, pdf)


      Fill me with random numbers using the probability distribution {pdf}


   .. method:: clone(self)


      Allocate a new vector and initialize it using my values


   .. method:: copy(self, other)


      Fill me with values from {other}, which is assumed to be of compatible shape


   .. method:: tuple(self)


      Build a representation of my contents as a tuple


   .. method:: view(self, start, shape)


      Build a view of my from {start} to {start+shape}


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


   .. method:: max(self)


      Compute my maximum value


   .. method:: min(self)


      Compute my maximum value


   .. method:: minmax(self)


      Compute my minimum and maximum values


   .. method:: sort(self)


      In-place sort of the elements of a vector


   .. method:: sortIndirect(self)


      Construct the permutation that would sort me in ascending order


   .. method:: shuffle(self, rng)


      Shuffle the elements
      :param rng: gsl.rng handle
      :return: self


   .. method:: mean(self, weights=None)


      Compute the mean value of my elements, weighted by the optional {weights}


   .. method:: median(self)


      Compute the median value of my elements; only works on previously sorted vectors


   .. method:: variance(self, mean=None)


      Compute the variance of my elements with respect to {mean}. If {mean} is {None}, it is
      computed on the fly


   .. method:: sdev(self, mean=None)


      Compute the mean value of my elements with respect to {mean}. If {mean} is {None}, it
      is computed on the fly


   .. method:: ndarray(self, copy=False)


      Return a numpy array reference (w/ shared data) if {copy} is False, or a new copy if {copy} is {True}


   .. method:: __len__(self)



   .. method:: __iter__(self)



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


   .. method:: _slice(self, index)


      Build a generator that yields the values described in the {index}



