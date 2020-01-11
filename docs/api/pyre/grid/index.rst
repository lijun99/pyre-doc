:mod:`pyre.grid`
================

.. py:module:: pyre.grid


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Grid/index.rst
   Tile/index.rst


Package Contents
----------------

.. py:class:: grid(shape, layout=None, value=None, data=None, **kwds)

   A logically cartesian grid

   .. method:: enumerate(self)


      Visit the entire grid in layout order returning ({index}, {value}) pairs


   .. method:: __getitem__(self, index)


      Return the value stored at {index}


   .. method:: __setitem__(self, index, value)


      Return the value stored at {index}


   .. method:: __len__(self)


      Compute my length



.. py:class:: tile(shape, layout=None, **kwds)

   Encapsulation of the shape and layout of the contents of a grid that enable the separation
   of the topological aspects of a grid from its memory layout

   Tiles are defined by providing two pieces of information

     - {shape}: a tuple of the extent of each grid index
     - {layout}: the packing order of the indices

   .. attribute:: shape
      :annotation: = []

      

   .. attribute:: layout
      :annotation: = []

      

   .. attribute:: size
      :annotation: = 0

      

   .. method:: offset(self, index)


      Compute the offset of the cell at the given {index} value


   .. method:: index(self, offset)


      Compute the index that corresponds to the given {offset}


   .. method:: visit(self, begin, end, layout)


      Generate a sequence of indices in the range {begin} to {end} in {layout} order


   .. method:: __getitem__(self, index)



   .. method:: __iter__(self)




