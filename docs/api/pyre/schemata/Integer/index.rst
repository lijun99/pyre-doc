:mod:`pyre.schemata.Integer`
============================

.. py:module:: pyre.schemata.Integer


Module Contents
---------------

.. py:class:: Integer(default=int(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for integers

   .. attribute:: typename
      :annotation: = int

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into an integer

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into an integer



