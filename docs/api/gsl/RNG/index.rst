:mod:`gsl.RNG`
==============

.. py:module:: gsl.RNG


Module Contents
---------------

.. py:class:: RNG(algorithm='ranlxs2', **kwds)

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



