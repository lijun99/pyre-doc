:mod:`gsl.Permutation`
======================

.. py:module:: gsl.Permutation


Module Contents
---------------

.. py:class:: Permutation(shape, data=None, **kwds)

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




