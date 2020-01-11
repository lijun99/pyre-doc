:mod:`pyre.constraints.Like`
============================

.. py:module:: pyre.constraints.Like


Module Contents
---------------

.. py:class:: Like(regexp, **kwds)

   Bases: :class:`pyre.constraints.Constraint.Constraint`

   Given a regular expression, a string satisfies this constraint if it matches the regular
   expression

   .. method:: validate(self, value, **kwds)


      Check whether {value} satisfies this constraint


   .. method:: __str__(self)




