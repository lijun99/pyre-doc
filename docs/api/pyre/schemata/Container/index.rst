:mod:`pyre.schemata.Container`
==============================

.. py:module:: pyre.schemata.Container


Module Contents
---------------

.. py:class:: Container(default=object, schema=Schema(), **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   The base class for type declarators that are sequences of other types

   .. attribute:: typename
      :annotation: = container

      

   .. method:: container(self)
      :property:


      The default container represented by this schema


   .. method:: coerce(self, value, **kwds)


      Convert {value} into an iterable



