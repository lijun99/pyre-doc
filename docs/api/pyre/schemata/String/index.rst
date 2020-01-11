:mod:`pyre.schemata.String`
===========================

.. py:module:: pyre.schemata.String


Module Contents
---------------

.. py:class:: String(default=str(), **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for strings

   .. attribute:: typename
      :annotation: = str

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a string

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a string



