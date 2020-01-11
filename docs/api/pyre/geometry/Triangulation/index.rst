:mod:`pyre.geometry.Triangulation`
==================================

.. py:module:: pyre.geometry.Triangulation


Module Contents
---------------

.. py:class:: Triangulation(grid, **kwds)

   A wrapper around a two dimensional grid that converts it into a simplicial mesh

   .. attribute:: grid
      

      

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



