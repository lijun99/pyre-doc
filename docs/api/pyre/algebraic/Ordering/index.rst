:mod:`pyre.algebraic.Ordering`
==============================

.. py:module:: pyre.algebraic.Ordering


Module Contents
---------------

.. py:class:: Ordering

   This is a mix-in class that traps comparisons

   The point is to redirect comparisons among instances of subclasses of {Ordering} to methods
   defined in these subclasses. These methods then build and return representations of the
   corresponding operators and their operands.

   {Ordering} expects its subclasses to define two class methods: {literal} and
   {operator}. The former is used to encapsulate operands that are not {Ordering}
   instances. The latter is used to construct the operator representations

   .. attribute:: __hash__
      

      

   .. method:: __eq__(self, other)



   .. method:: __ne__(self, other)



   .. method:: __le__(self, other)



   .. method:: __ge__(self, other)



   .. method:: __lt__(self, other)



   .. method:: __gt__(self, other)




