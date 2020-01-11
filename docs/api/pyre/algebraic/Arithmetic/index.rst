:mod:`pyre.algebraic.Arithmetic`
================================

.. py:module:: pyre.algebraic.Arithmetic


Module Contents
---------------

.. py:class:: Arithmetic

   This is a mix-in class that traps the arithmetic operators relevant for numeric types

   The point is to redirect arithmetic among instances of subclasses of {Arithmetic} to
   methods defined in these subclasses. These methods then build and return representations of
   the corresponding operators and their operands.

   {Arithmetic} expects its subclasses to define two class methods: {literal} and
   {operator}. The former is used to encapsulate operands that are not {Arithmetic}
   instances. The latter is used to construct the operator representations

   .. method:: __add__(self, other)



   .. method:: __sub__(self, other)



   .. method:: __mul__(self, other)



   .. method:: __truediv__(self, other)



   .. method:: __floordiv__(self, other)



   .. method:: __mod__(self, other)



   .. method:: __pow__(self, other)



   .. method:: __pos__(self)



   .. method:: __neg__(self)



   .. method:: __abs__(self)



   .. method:: __radd__(self, other)



   .. method:: __rsub__(self, other)



   .. method:: __rmul__(self, other)



   .. method:: __rtruediv__(self, other)



   .. method:: __rfloordiv__(self, other)



   .. method:: __rmod__(self, other)



   .. method:: __rpow__(self, other)




