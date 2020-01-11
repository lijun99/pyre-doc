:mod:`pyre.constraints.Between`
===============================

.. py:module:: pyre.constraints.Between


Module Contents
---------------

.. py:class:: Between(low, high, **kwds)

   Bases: :class:`pyre.constraints.Constraint.Constraint`

   Given {a} and {b} from a set with an ordering principle, this constraint is satisfied if
   the candidate is in {(a,b)}

   .. method:: validate(self, value, **kwds)


      Check whether {candidate} satisfies this constraint


   .. method:: __str__(self)




