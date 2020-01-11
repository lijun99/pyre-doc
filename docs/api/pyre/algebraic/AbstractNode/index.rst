:mod:`pyre.algebraic.AbstractNode`
==================================

.. py:module:: pyre.algebraic.AbstractNode


Module Contents
---------------

.. py:class:: AbstractNode

   The base class for hierarchies that implement the algebraic protocol

   The mix-in classes {Arithmetic}, {Ordering} and {Boolean} overload the methods that are invoked
   by the evaluation of expressions involving python operators. The implementation of these
   methods expect {AbstractNode} subclasses to provide access to two subclasses, {Literal} and
   {Operator}, that are used to build a representation of the python expression. {Literal} is
   used to encapsulate objects that are foreign to the {Node} class hierarchy, e.g. integers,
   and {Operation} encodes the operator encountered and its operands. This access must be
   provided through two {Node} properties, {literal} and {operation}, which provide an extra
   layer of abstraction by hiding the actual {Node} subclasses.

   .. attribute:: leaf
      

      

   .. attribute:: composite
      

      

   .. attribute:: literal
      

      

   .. attribute:: variable
      

      

   .. attribute:: operator
      

      

   .. attribute:: _pyre_hasAlgebra
      :annotation: = False

      

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


   .. method:: cyclic(self)


      Determine whether my subgraph has any cycles


   .. method:: replace(self, obsolete)


      Take ownership of any information held by the {obsolete} node, which is about to be
      destroyed


   .. method:: dump(self, name, indent)




