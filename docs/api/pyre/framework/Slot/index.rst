:mod:`pyre.framework.Slot`
==========================

.. py:module:: pyre.framework.Slot


Module Contents
---------------

.. py:class:: Slot(key=None, **kwds)

   Bases: :class:`pyre.framework.Dashboard.Dashboard`

   This class provides centralized access to the values of all configurables

   All configuration information recovered from the command line, configuration files or
   explicit assignments to the {configurator} is stored in slots. The {configurator} maintains
   a map from the hashed version of a public name to a slot.

   Similarly, all component classes and instances store the values of their properties and
   facilities in slots. The {pyre_inventory} dictionary is a map from trait descriptors to the
   corresponding slot, and the {__get__} and {__set__} descriptor methods manipulate the slot
   contents.

   Component classes and instances with public names register their slots with the
   {configurator}, which establishes the connection between component configurable state and
   the configuration store. These slots are shared among the component and the store, and
   changes to one are immediately reflected in the other.

   In addition, slots manage the trait values by walking them through coercions and
   validations whenever a value change is detected.

   In order to allow configuration assignments to properly override existing values, slots
   maintain the notion of the priority of their current value. This way clients can check
   whether the incoming value may or may not override the existing one. This frees the
   framework from having to guarantee that the configuration store is visited in some fixed
   order.

   Slots also maintain a locator, an indication of the source of the configuration information
   that was used to set the value of the trait.

   .. py:class:: literal(key=None, **kwds)

      Representation of foreign values


   .. attribute:: key
      

      

   .. method:: model(self)
      :property:


      Return the model against which named references are resolved


   .. method:: name(self)
      :property:


      Get the name under which I am registered with the nameserver



