:mod:`pyre.constraints.Not`
===========================

.. py:module:: pyre.constraints.Not


Module Contents
---------------

.. py:class:: Not(constraint, **kwds)

   Bases: :class:`pyre.constraints.Constraint.Constraint`

   Constraint that is satisfied when the candidate fails to satisfy a given constraint

   .. method:: validate(self, value, **kwds)


      Check whether {value} satisfies this constraint


   .. method:: __str__(self)




