:mod:`pyre.schemata.Complex`
============================

.. py:module:: pyre.schemata.Complex


Module Contents
---------------

.. py:class:: Complex(default=complex(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for complex numbers

   .. attribute:: typename
      :annotation: = complex

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a complex number

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a complex number



