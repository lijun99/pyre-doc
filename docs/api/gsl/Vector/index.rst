:mod:`gsl.Vector`
=================

.. py:module:: gsl.Vector


Module Contents
---------------

.. py:class:: Vector(shape, data=None, **kwds)

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



