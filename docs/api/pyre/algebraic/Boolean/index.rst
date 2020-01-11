:mod:`pyre.algebraic.Boolean`
=============================

.. py:module:: pyre.algebraic.Boolean


Module Contents
---------------

.. py:class:: Boolean

   This is a mix-in class that traps the boolean operators

   The point is to redirect boolean operations among instances of subclasses of {Boolean} to
   methods defined in these subclasses. These methods then build and return representations of
   the corresponding operators and their operands.

   {Boolean} expects its subclasses to define two class methods: {literal} and
   {operator}. The former is used to encapsulate operands that are not {Boolean}
   instances. The latter is used to construct the operator representations.

   .. method:: __and__(self, other)



   .. method:: __or__(self, other)



   .. method:: __rand__(self, other)



   .. method:: __ror__(self, other)




