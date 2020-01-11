:mod:`pyre.grid.Grid`
=====================

.. py:module:: pyre.grid.Grid


Module Contents
---------------

.. py:class:: Grid(shape, layout=None, value=None, data=None, **kwds)

   A logically cartesian grid

   .. method:: enumerate(self)


      Visit the entire grid in layout order returning ({index}, {value}) pairs


   .. method:: __getitem__(self, index)


      Return the value stored at {index}


   .. method:: __setitem__(self, index, value)


      Return the value stored at {index}


   .. method:: __len__(self)


      Compute my length



