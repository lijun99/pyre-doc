:mod:`pyre.constraints.Subset`
==============================

.. py:module:: pyre.constraints.Subset


Module Contents
---------------

.. py:class:: Subset(choices, **kwds)

   Bases: :class:`pyre.constraints.Constraint.Constraint`

   Constraint that is satisfied when the candidate is a subset of a given set

   .. method:: validate(self, value, **kwds)


      Check whether {value} satisfies this constraint


   .. method:: __str__(self)




