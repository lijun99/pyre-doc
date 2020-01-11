:mod:`pyre.components.PublicInventory`
======================================

.. py:module:: pyre.components.PublicInventory


Module Contents
---------------

.. py:class:: PublicInventory(key, **kwds)

   Bases: :class:`pyre.components.Inventory.Inventory`

   Strategy for providing access to the state of component classes and instances that were
   given a publicly visible name and use slots managed the pyre nameserver for storage.

   .. method:: name(self)
      :property:


      Look up the family name of my client


   .. method:: fragments(self)
      :property:


      Look up the family name of my client


   .. method:: package(self)
      :property:


      Return the package associated with this client


   .. method:: setTraitValue(self, trait, **kwds)


      Set the value of the slot associated with the given {trait} descriptor


   .. method:: getTraitValue(self, trait)


      Get the value associated with this {trait} descriptor


   .. method:: getTraitLocator(self, trait)


      Get the location of last assignment for this {trait}


   .. method:: getTraitPriority(self, trait)


      Retrieve the priority of the last assignment for this {trait}


   .. method:: getSlots(self)


      Return an iterable over the trait value storage


   .. method:: initializeClass(cls, component, family, **kwds)
      :classmethod:


      Build inventory appropriate for a component instance that has a publicly visible name and
      is registered with the nameserver


   .. method:: initializeInstance(cls, instance, name)
      :classmethod:


      Build inventory appropriate for a component instance that has a publicly visible name and
      is registered with the nameserver


   .. method:: localSlots(cls, key, component)
      :classmethod:


      Build slots for the locally declared traits of a {component} class


   .. method:: inheritedSlots(cls, key, component)
      :classmethod:


      Build slots for the inherited traits of a {component} class


   .. method:: instanceSlots(cls, key, instance)
      :classmethod:


      Build slots for the initial inventory of an instance by building references to all the
      slots in the inventory of its class


   .. method:: registerSlots(cls, key, slots, locator)
      :classmethod:


      Go through the (trait, factory, value) tuples in {slots} and register them with the
      nameserver


   .. method:: __getitem__(self, trait)


      Retrieve the slot associated with {trait}


   .. method:: __str__(self)




