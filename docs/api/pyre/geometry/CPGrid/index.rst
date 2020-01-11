:mod:`pyre.geometry.CPGrid`
===========================

.. py:module:: pyre.geometry.CPGrid


Module Contents
---------------

.. py:class:: CPGrid(*args, **kwds)

   Bases: :class:`pyre.geometry.Grid.Grid`

   A corner point grid is a collection of hexahedral cells each of which is defined by the
   corners of two of its faces

   .. method:: dimension(self)
      :property:


      Compute the dimension of space


   .. method:: numberOfPoints(self)
      :property:


      Compute the number of nodes in the grid


   .. method:: numberOfCells(self)
      :property:


      Compute the total number of cells in the grid


   .. method:: points(self)
      :property:


      Return an iterator over all the nodes in the grid


   .. method:: cells(self)
      :property:


      Return an iterator over the connectivity of my grid


   .. method:: cell(self, corners)


      Create a cell out of the coordinates of its eight corners


   .. method:: boundingBox(self)


      Compute the bounding box of the grid


   .. method:: eigenlen(self)


      Compute the characteristic scale of the mesh


   .. method:: scale(self, idx, cell, dim, inf)


      Compute the smallest edge in {cell}


   .. method:: verify(self)


      Run some consistency checks



