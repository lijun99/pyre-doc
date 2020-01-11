:mod:`pyre.patterns.Printer`
============================

.. py:module:: pyre.patterns.Printer


Module Contents
---------------

.. py:class:: Printer(format=None, **kwds)

   Bases: :class:`pyre.patterns.CoFunctor.CoFunctor`

   A coroutine that sends a textual representation of the values it receives to {stdout}

   .. method:: throw(self, errorTp, error=None, traceback=None)


      Handle exceptions


   .. method:: __call__(self)


      Store everything that comes in



