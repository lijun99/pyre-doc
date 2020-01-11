:mod:`pyre.algebraic.Composite`
===============================

.. py:module:: pyre.algebraic.Composite


Module Contents
---------------

.. py:class:: Composite(operands, **kwds)

   Mix-in class that provides an implementation of the subset of the interface of {Node} that
   requires traversal of the expression graph rooted at nodes with dependencies.

   This class assumes that its instances provide {operands}, a tuple of their dependencies on
   other nodes

   .. method:: operands(self)
      :property:


      A sequence of my direct dependents


   .. method:: span(self)
      :property:


      Return a sequence over my entire dependency graph


   .. method:: literals(self)
      :property:


      Return a sequence over the nodes in my dependency graph that encapsulate foreign objects


   .. method:: operators(self)
      :property:


      Return a sequence over the composite nodes in my dependency graph


   .. method:: variables(self)
      :property:


      Return a sequence over the leaf nodes in my dependency graph


   .. method:: substitute(self, current, replacement, clean=None)


      Traverse my span and replace all occurrences of {current} with {replacement}

      This method makes it possible to introduce cycles in the dependency graph, which is not
      desirable typically. To prevent this, we check that {self} is not in the span of
      {replacement} when the caller does not supply a set of {clean} nodes


   .. method:: _substitute(self, current, replacement)


      Adjust the operands by substituting {replacement} for {current} in the sequence of operands



