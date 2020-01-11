:mod:`pyre.calc.NodeInfo`
=========================

.. py:module:: pyre.calc.NodeInfo


Module Contents
---------------

.. py:class:: NodeInfo(key=None, name=None, split=None, **kwds)

   The base class for nodal metadata maintained by symbol tables

   .. attribute:: key
      

      

   .. attribute:: name
      

      

   .. attribute:: split
      

      

   .. method:: fillNodeId(model, key=None, name=None, split=None)
      :staticmethod:


      Given one of the three representations of the key of a node in {model}, reconstruct all of
      them so clients can choose whichever representation fits their needs



