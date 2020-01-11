:mod:`pyre.calc.Memo`
=====================

.. py:module:: pyre.calc.Memo


Module Contents
---------------

.. py:class:: Memo

   A mix-in class that implements value memoization

   .. attribute:: dirty
      :annotation: = True

      

   .. attribute:: _value
      

      

   .. method:: getValue(self, **kwds)


      Override the node value retriever and return the contents of my value cache if it is up
      to date; otherwise, recompute the value and update the cache


   .. method:: setValue(self, value, **kwds)


      Override the value setter to refresh my cache and notify my observers


   .. method:: flush(self, **kwds)


      Invalidate my cache and notify my observers



