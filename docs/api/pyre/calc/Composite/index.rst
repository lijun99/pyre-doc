:mod:`pyre.calc.Composite`
==========================

.. py:module:: pyre.calc.Composite


Module Contents
---------------

.. py:class:: Composite

   Mix-in class that augments raph traversal for the new leaves defined in this package

   .. method:: expressions(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are constructed out of python
      expressions involving the names of other nodes


   .. method:: interpolations(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are constructed by expanding
      the values of other nodes in a macro


   .. method:: mappings(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are mappings


   .. method:: references(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are references to other nodes


   .. method:: sequences(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are sequences


   .. method:: uresolveds(self)
      :property:


      Return a sequence over the unresolved nodes in my dependency graph



