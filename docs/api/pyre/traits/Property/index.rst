:mod:`pyre.traits.Property`
===========================

.. py:module:: pyre.traits.Property


Module Contents
---------------

.. py:class:: Property(classSlot=None, instanceSlot=None, **kwds)

   Bases: :class:`pyre.traits.Slotted.Slotted`

   The base class for traits that correspond to simple types

   .. py:class:: schema

      Mixin for handling generic values

      .. method:: macro(self)
         :property:


         The default strategy for handling macros in slot values


      .. method:: native(self)
         :property:


         The strategy for building slots from more complex input values



   .. py:class:: numeric

      Mixin for handling numeric types

      .. method:: macro(self)
         :property:


         Access to the default strategy for handling macros for numeric types



   .. py:class:: sequences

      Mixin for handling typed containers

      .. method:: macro(self)
         :property:


         The default strategy for handling slot values that are strings and therefore
         subject to some kind of evaluation in the context of the configuration store


      .. method:: native(self, value, **kwds)


         The strategy for building slots from more complex input values



   .. attribute:: category
      :annotation: = property

      

   .. attribute:: isProperty
      :annotation: = True

      

   .. method:: __str__(self)




