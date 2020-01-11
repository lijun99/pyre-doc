:mod:`pyre.geometry.Octree`
===========================

.. py:module:: pyre.geometry.Octree


Module Contents
---------------

.. py:class:: Octree(intervals, **kwds)

   A dimension independent implementation of the octree family of spatial data structures

   .. method:: contains(self, point)


      Determine whether {point} falls within my box


   .. method:: insert(self, point, level=0)


      Insert {point} within this box, creating any children necessary


   .. method:: subdivide(self)


      Convert me from a leaf node to an internal one. This version build all children
      regardless of whether they end up containing points


   .. method:: hash(self, point)


      Figure out within which of my children {point} falls



