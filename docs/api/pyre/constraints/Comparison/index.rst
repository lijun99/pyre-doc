:mod:`pyre.constraints.Comparison`
==================================

.. py:module:: pyre.constraints.Comparison


Module Contents
---------------

.. py:class:: Comparison(value, **kwds)

   Bases: :class:`pyre.constraints.Constraint.Constraint`

   Base class for constraints that compare candidates against values

   .. attribute:: tag
      

      

   .. attribute:: compare
      

      

   .. method:: validate(self, value, **kwds)


      Check whether {value} satisfies this constraint


   .. method:: __str__(self)




