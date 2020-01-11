:mod:`pyre.traits.Facility`
===========================

.. py:module:: pyre.traits.Facility


Module Contents
---------------

.. py:class:: Facility(protocol, **kwds)

   Bases: :class:`pyre.traits.Slotted.Slotted`, :class:`pyre.schemata.component`

   The descriptor for traits that are components

   .. attribute:: category
      :annotation: = component

      

   .. attribute:: isFacility
      :annotation: = True

      

   .. method:: default(self)
      :property:


      Access to my default value


   .. method:: macro(self, **kwds)


      Return the default strategy for handling expressions in slot values


   .. method:: native(self, **kwds)


      The strategy for building slots from more complex input values


   .. method:: instantiate(self, value, node, incognito=False, **kwds)


      Coerce {value} into an instance of a component compatible with my protocol


   .. method:: __str__(self)




