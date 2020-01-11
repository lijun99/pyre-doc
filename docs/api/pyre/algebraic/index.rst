:mod:`pyre.algebraic`
=====================

.. py:module:: pyre.algebraic


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   AbstractNode/index.rst
   Algebra/index.rst
   Arithmetic/index.rst
   Boolean/index.rst
   Composite/index.rst
   Leaf/index.rst
   Literal/index.rst
   Operator/index.rst
   Ordering/index.rst
   Variable/index.rst
   exceptions/index.rst


Package Contents
----------------

.. py:class:: algebra

   Bases: :class:`pyre.patterns.AbstractMetaclass.AbstractMetaclass`

   Metaclass that endows its instances with algebraic structure

   .. method:: leafDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of literals


   .. method:: compositeDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of literals


   .. method:: literalDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of literals


   .. method:: operatorDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of operators


   .. method:: variableDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of variables


   .. method:: isIgnorable(cls, bases)
      :classmethod:


      Filter that determines whether a class should be decorated or not.

      This is necessary because the metaclass is asked to process all subclasses of the type
      that injected it in the hierarchy. In our case, variables, operators and the like would
      also pass through the process. This routine detects these cases and avoids them



.. py:class:: node

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




