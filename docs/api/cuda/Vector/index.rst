:mod:`cuda.Vector`
==================

.. py:module:: cuda.Vector


Module Contents
---------------

.. py:class:: Vector(shape=1, source=None, dtype='float64', **kwds)

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



