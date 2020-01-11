:mod:`pyre.db.expressions`
==========================

.. py:module:: pyre.db.expressions


Module Contents
---------------

.. py:class:: UnaryPostfix(operand, **kwds)

   The base class for postfix unary expression factories

   .. attribute:: operand
      

      

   .. attribute:: operator
      

      

   .. method:: sql(self)


      SQL rendering of the expression I represent



.. py:class:: IsNull

   Bases: :class:`pyre.db.expressions.UnaryPostfix`

   A node factory that takes a field reference {op} and builds the expression {op IS NULL}

   .. attribute:: operator
      :annotation: = IS NULL

      


.. py:class:: IsNotNull

   Bases: :class:`pyre.db.expressions.UnaryPostfix`

   A node factory that takes a field reference {op} and builds the expression {op IS NOT NULL}

   .. attribute:: operator
      :annotation: = IS NOT NULL

      


.. py:class:: Cast(field, targetType, **kwds)

   Implementation of the {CAST} expression

   .. method:: sql(self, **kwds)


      SQL rendering of the expression I represent



.. py:class:: Like(field, regex, **kwds)

   Implementation of the LIKE operator

   .. method:: sql(self, **kwds)


      SQL rendering of the expression I represent



