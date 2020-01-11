:mod:`pyre.geometry.Grid`
=========================

.. py:module:: pyre.geometry.Grid


Module Contents
---------------

.. py:class:: Grid(shape=(), packing=ROW_MAJOR, *args, **kwds)

   Bases: :class:`list`

   A logically Cartesian grid implemented as a list with a custom indexing function

   .. attribute:: ROW_MAJOR
      :annotation: = row-major

      

   .. attribute:: COLUMN_MAJOR
      :annotation: = column-major

      

   .. method:: dimension(self)
      :property:


      Compute the dimension of space


   .. method:: numberOfPoints(self)
      :property:


      Compute the number of nodes in the grid


   .. method:: numberOfCells(self)
      :property:


      Compute the number of cells in the grid


   .. method:: points(self)
      :property:


      Return an iterator over the nodes in my grid


   .. method:: cells(self)
      :property:


      Return an iterator over the connectivity of the grid


   .. method:: boundingBox(self)


      Compute the bounding box of the grid


   .. method:: __getitem__(self, index)


      Support structured access to the cells


   .. method:: columnMajor(self, index)


      Convert the {index} into an offset using column-major format


   .. method:: rowMajor(self, index)


      Convert the {index} into an offset using row-major format


   .. method:: verify(self)


      Run some simple diagnostics


   .. method:: anchors(self)


      Compute the grid index of the corner of each cell


   .. method:: describeCellAt(self, anchor)


      Build a pair of indices for each coordinate that can be used to visit the corners of a grid
      cell in counter clockwise fashion


   .. method:: cornersOfCellAt(self, anchor)


      Visit the corners of the cell at {anchor} in a counter clockwise fashion



