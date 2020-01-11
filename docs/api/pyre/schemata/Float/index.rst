:mod:`pyre.schemata.Float`
==========================

.. py:module:: pyre.schemata.Float


Module Contents
---------------

.. py:class:: Float(default=float(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for floats

   .. attribute:: typename
      :annotation: = float

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a float

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a float



