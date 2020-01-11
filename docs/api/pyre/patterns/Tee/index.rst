:mod:`pyre.patterns.Tee`
========================

.. py:module:: pyre.patterns.Tee


Module Contents
---------------

.. py:class:: Tee

   Bases: :class:`pyre.patterns.CoFunctor.CoFunctor`, :class:`list`

   A coroutine that accumulates data in a container

   .. method:: throw(self, errorTp, error=None, traceback=None)


      Raise an exception


   .. method:: close(self)


      Shut things down


   .. method:: __call__(self)


      Store everything that comes in



