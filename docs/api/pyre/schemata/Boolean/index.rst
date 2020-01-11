:mod:`pyre.schemata.Boolean`
============================

.. py:module:: pyre.schemata.Boolean


Module Contents
---------------

.. py:class:: Boolean(default=True, **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for booleans

   .. attribute:: typename
      :annotation: = bool

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} to bool

      

   .. attribute:: xlat
      

      

   .. method:: coerce(self, value, **kwds)


      Convert {value} into a boolean



