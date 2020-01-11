:mod:`pyre.constraints.Or`
==========================

.. py:module:: pyre.constraints.Or


Module Contents
---------------

.. py:class:: Or(*constraints, **kwds)

   Bases: :class:`pyre.constraints.Constraint.Constraint`

   Given a set of constraints, a candidate satisfies this iff it satisfies any of the constraints

   .. method:: validate(self, value, **kwds)


      Check whether {value} satisfies this constraint


   .. method:: __str__(self)




