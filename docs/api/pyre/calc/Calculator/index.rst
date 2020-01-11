:mod:`pyre.calc.Calculator`
===========================

.. py:module:: pyre.calc.Calculator


Module Contents
---------------

.. py:class:: Calculator

   Bases: :class:`pyre.algebraic.algebra`

   Metaclass that grants nodes value management capabilities

   .. method:: literalDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of literals


   .. method:: variableDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of literals


   .. method:: operatorDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of operators


   .. method:: sequenceDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of operators


   .. method:: mappingDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of operators


   .. method:: expressionDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of expressions


   .. method:: interpolationDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of interpolations


   .. method:: referenceDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of references


   .. method:: unresolvedDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of unresolved nodes


   .. method:: managedDependencyDerivation(cls)
      :classmethod:


      Build the canonical derivation of node that other nodes can depend on


   .. method:: managedDependentDerivation(cls)
      :classmethod:


      Place {dependent} in the right spot in the inheritance graph of {record}


   .. method:: managedCompositeDerivation(cls, composite, record)
      :classmethod:


      Place the class {composite} in the right spot in the {record} inheritance graph



