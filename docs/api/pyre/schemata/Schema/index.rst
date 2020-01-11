:mod:`pyre.schemata.Schema`
===========================

.. py:module:: pyre.schemata.Schema


Module Contents
---------------

.. py:class:: Schema(default=None, **kwds)

   The base class for type declarators

   .. attribute:: typename
      :annotation: = identity

      

   .. method:: default(self)
      :property:


      Grant access to my default value


   .. method:: coerce(self, value, **kwds)


      Convert the given value into a python native object


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



