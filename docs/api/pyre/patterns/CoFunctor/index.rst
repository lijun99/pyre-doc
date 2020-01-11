:mod:`pyre.patterns.CoFunctor`
==============================

.. py:module:: pyre.patterns.CoFunctor


Module Contents
---------------

.. py:class:: CoFunctor(*args, **kwds)

   Converts a functor into a coroutine

   .. method:: send(self, value)


      Accept a value


   .. method:: throw(self, errorTp, error=None, traceback=None)


      Raise an exception


   .. method:: close(self)


      Shut things down


   .. method:: __next__(self)


      Advance



