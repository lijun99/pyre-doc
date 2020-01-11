:mod:`pyre.weaver.Expression`
=============================

.. py:module:: pyre.weaver.Expression


Module Contents
---------------

.. py:class:: Expression(nodeType=None, **kwds)

   This mill mix-in builds textual representations of expression trees built out of node
   hierarchies that conform to the {pyre.algebraic} protocols. The base class of the node
   hierarchy must be supplied as a constructor argument; the implementation falls back to
   {pyre.calc.Node} if no alternative is provided.

   .. method:: expression(self, root, **kwds)


      Build a representation of {node}, assumed to be an instance of a {pyre.calc.Node}
      subclass


   .. method:: _newSymbolTable(self)


      Build a table mapping all {pyre.calc} operators to their 'default' symbols

      This table is built by considering the python representation of the operator to be its
      default. Other mills can build their own tables, or start with this one and modify it as
      needed


   .. method:: _newRenderingStrategyTable(self, nodeType)


      Build a table that maps {pyre.calc} operators to rendering strategies


   .. method:: _literalRenderer(self, node, **kwds)


      Render {node} as a literal


   .. method:: _operatorRenderer(self, node, **kwds)


      Render {node} assuming it is an operation of some kind


   .. method:: _binaryOperatorRenderer(self, node, **kwds)


      Render {node} assuming it is an operator


   .. method:: _unaryOperatorRenderer(self, node, **kwds)


      Render {node} assuming it is an operator whose evaluator has a registered symbol


   .. method:: _oppositeRenderer(self, node, **kwds)


      Render the absolute value of {node}



