:mod:`pyre.records.Mutable`
===========================

.. py:module:: pyre.records.Mutable


Module Contents
---------------

.. py:class:: Mutable

   Bases: :class:`pyre.records.NamedTuple.NamedTuple`

   Storage for and access to the values of mutable record instances

   This class assumes that its items are {pyre.calc} nodes.

   .. attribute:: __slots__
      :annotation: = []

      

   .. method:: __getitem__(self, index)


      Retrieve the item at {index} and return its value


   .. method:: __setitem__(self, index, value)


      Set the item at {index} to the indicated value


   .. method:: __iter__(self)


      Build an iterator over my values



