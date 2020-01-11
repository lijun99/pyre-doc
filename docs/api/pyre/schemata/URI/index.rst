:mod:`pyre.schemata.URI`
========================

.. py:module:: pyre.schemata.URI


Module Contents
---------------

.. py:class:: URI(default=locator(), scheme=None, authority=None, address=None, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   Parser for resource identifiers

   .. attribute:: typename
      :annotation: = uri

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a URI

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a resource locator


   .. method:: json(self, value)


      Generate a JSON representation of {value}



