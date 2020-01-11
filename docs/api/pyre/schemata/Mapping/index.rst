:mod:`pyre.schemata.Mapping`
============================

.. py:module:: pyre.schemata.Mapping


Module Contents
---------------

.. py:class:: Mapping

   Bases: :class:`pyre.schemata.Container.Container`

   The base class for type declarators that map strings to other types

   .. attribute:: typename
      :annotation: = mapping

      

   .. attribute:: container
      

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} to a mapping

      

   .. method:: _coerce(self, value, **kwds)


      Convert {value} into a container



