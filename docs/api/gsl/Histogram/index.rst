:mod:`gsl.Histogram`
====================

.. py:module:: gsl.Histogram


Module Contents
---------------

.. py:class:: Histogram(bins, data=None, **kwds)

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



