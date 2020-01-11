:mod:`pyre.patterns.Accumulator`
================================

.. py:module:: pyre.patterns.Accumulator


Module Contents
---------------

.. py:class:: Accumulator(**kwds)

   Bases: :class:`pyre.patterns.CoFunctor.CoFunctor`

   A coroutine that accumulates data in a container

   .. method:: throw(self, errorTp, error=None, traceback=None)


      Handle exceptions


   .. method:: __call__(self)


      Store everything that comes in



