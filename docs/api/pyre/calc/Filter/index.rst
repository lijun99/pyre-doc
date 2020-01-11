:mod:`pyre.calc.Filter`
=======================

.. py:module:: pyre.calc.Filter


Module Contents
---------------

.. py:class:: Filter(constraints=None, **kwds)

   A mix-in class that changes the values of nodes iff they pass its constraints

   .. method:: setValue(self, **kwds)


      Override the value setter to let the assignment go through iff my constraints are all
      satisfied



