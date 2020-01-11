:mod:`pyre.algebraic.Algebra`
=============================

.. py:module:: pyre.algebraic.Algebra


Module Contents
---------------

.. py:class:: Algebra

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



