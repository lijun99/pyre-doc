:mod:`pyre.schemata.Component`
==============================

.. py:module:: pyre.schemata.Component


Module Contents
---------------

.. py:class:: Component(protocol, default=default, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for components

   .. attribute:: default
      

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a component

      

   .. attribute:: protocol
      

      

   .. method:: typename(self)
      :property:


      Identify my schema through my protocol


   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a component class compatible with my protocol


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



