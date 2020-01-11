:mod:`pyre.geometry.Mesh`
=========================

.. py:module:: pyre.geometry.Mesh


Module Contents
---------------

.. py:class:: Mesh(**kwds)

   A simple representation of a simplicial mesh that maintains a database of points and
   connectivities

   .. method:: dimension(self)
      :property:


      Infer the dimension of space


   .. method:: numberOfPoints(self)
      :property:


      Compute the number of points in the mesh


   .. method:: numberOfCells(self)
      :property:


      Compute the number of elements in the mesh


   .. method:: cells(self)
      :property:


      Build an iterator over my simplices


   .. method:: point(self, coordinates)


      Create a point at the given location


   .. method:: simplex(self, nodes)


      Add the given simplex specification to my pile



