:mod:`pyre.schemata.Decimal`
============================

.. py:module:: pyre.schemata.Decimal


Module Contents
---------------

.. py:class:: Decimal(default=decimal.Decimal(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for fixed point numbers

   .. attribute:: typename
      :annotation: = decimal

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a decimal


   .. method:: json(self, value)


      Generate a JSON representation of {value}



