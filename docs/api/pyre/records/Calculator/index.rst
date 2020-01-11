:mod:`pyre.records.Calculator`
==============================

.. py:module:: pyre.records.Calculator


Module Contents
---------------

.. py:class:: Calculator

   A strategy for pulling data from a stream that attaches the values to {pyre.calc} nodes,
   making the record instances mutable

   .. method:: __call__(self, record, source, **kwds)


      Pull values from {source}, convert and yield them



