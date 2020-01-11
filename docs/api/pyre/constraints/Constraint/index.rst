:mod:`pyre.constraints.Constraint`
==================================

.. py:module:: pyre.constraints.Constraint


Module Contents
---------------

.. py:class:: Constraint

   The base class for constraints

   .. method:: validate(self, value, **kwds)


      The default behavior for constraints is to raise a ConstraintViolationError.

      Override to implement a specific test


   .. method:: __call__(self, value, **kwds)


      Interface to make constraints callable


   .. method:: __and__(self, other)


      Enable the chaining of constraints using the logical operators


   .. method:: __or__(self, other)


      Enable the chaining of constraints using the logical operators



