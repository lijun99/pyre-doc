:mod:`pyre.components.PrivateInventory`
=======================================

.. py:module:: pyre.components.PrivateInventory


Module Contents
---------------

.. py:class:: PrivateInventory

   Bases: :class:`pyre.components.Inventory.Inventory`

   Strategy for managing the state of component classes and instances that were not given a
   publicly visible name, hence they are responsible for managing their own private state

   .. attribute:: key
      

      

   .. method:: setTraitValue(self, trait, factory, value, **kwds)


      Set the value of the slot associated with {trait}


   .. method:: getTraitValue(self, trait)


      Get the value associated with this {trait} descriptor


   .. method:: getTraitLocator(self, trait)


      Retrieve the location of the last assignment for this {trait}


   .. method:: getTraitPriority(self, trait)


      Retrieve the priority of the last assignment for this {trait}


   .. method:: getSlots(self)


      Return an iterable over the trait value storage


   .. method:: initializeClass(cls, component, **kwds)
      :classmethod:


      Build inventory appropriate for a component class that is not registered with the
      nameserver


   .. method:: initializeInstance(cls, instance, **kwds)
      :classmethod:


      Build inventory appropriate for a component instance that is not registered with the
      nameserver


   .. method:: localSlots(cls, component)
      :classmethod:


      Build slots for the locally declared traits of a {component} class


   .. method:: inheritedSlots(cls, component)
      :classmethod:


      Build slots for the inherited traits of a {component} class


   .. method:: instanceSlots(cls, instance)
      :classmethod:


      Build slots for the initial inventory of an instance by building references to all the
      slots in the inventory of its class


   .. method:: __str__(self)




