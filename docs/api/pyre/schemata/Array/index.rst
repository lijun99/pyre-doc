:mod:`pyre.schemata.Array`
==========================

.. py:module:: pyre.schemata.Array


Module Contents
---------------

.. py:class:: Array(default=(), **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   The array type declarator

   .. attribute:: typename
      :annotation: = array

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} to an array

      

   .. method:: coerce(self, value, **kwds)


      Convert {value} into a tuple



