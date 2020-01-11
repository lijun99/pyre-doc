:mod:`pyre.geometry`
====================

.. py:module:: pyre.geometry


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   CPGrid/index.rst
   Field/index.rst
   Grid/index.rst
   Mesh/index.rst
   Octree/index.rst
   Point/index.rst
   PointCloud/index.rst
   Simplex/index.rst
   SimplicialMesh/index.rst
   Surface/index.rst
   Triangulation/index.rst


Package Contents
----------------

.. function:: surface(**kwds)

   Create a surface


.. function:: grid(**kwds)

   Create a grid


.. function:: cpg(**kwds)

   Create a corner point grid


.. function:: mesh(**kwds)

   Create a mesh


.. function:: field(**kwds)

   Create a field over a one of the space discretizations


.. function:: triangulation(**kwds)

   Create a triangulation


.. function:: transfer(grid, fields, mesh)

   Transfer the {fields} defined over a grid to fields defined over the {mesh}


.. function:: boxUnion(b1, b2)

   Compute a box big enough to contain both input boxes


.. function:: boxIntersection(b1, b2)

   Compute a box small enough  to fit inside both input boxes


.. function:: convexHull(points)

   Compute the convex hull of the given {points}


