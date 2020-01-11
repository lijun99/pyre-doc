:mod:`pyre.components.Component`
================================

.. py:module:: pyre.components.Component


Module Contents
---------------

.. py:class:: Component(name, locator, **kwds)

   Bases: :class:`pyre.components.Configurable.Configurable`

   The base class for all components

   .. attribute:: pyre_inventory
      

      

   .. attribute:: pyre_implements
      

      

   .. attribute:: pyre_isComponent
      :annotation: = True

      

   .. method:: pyre_key(self)
      :property:


      Look up my key


   .. method:: pyre_name(self)
      :property:


      Look up my name


   .. method:: pyre_family(cls)
      :classmethod:


      Deduce my family name


   .. method:: pyre_familyFragments(cls)
      :classmethod:


      Deduce my family name


   .. method:: pyre_spec(self)
      :property:


      Build my configuration specification


   .. method:: pyre_normalizeInstanceName(cls, name)
      :classmethod:


      Give a component a chance to normalize the {name} of an instance that is about to
      be created


   .. method:: pyre_package(cls)
      :classmethod:


      Deduce my package name


   .. method:: pyre_isPublicClass(cls)
      :classmethod:


      Check whether this component class is public


   .. method:: pyre_public(cls)
      :classmethod:


      Generate the sequence of my public ancestors, i.e. the ones that have a non-trivial family


   .. method:: pyre_setTrait(self, alias, value, priority=None, locator=None)


      Assign {value} to the trait named {alias}


   .. method:: pyre_getTrait(self, alias)


      Retrieve the value and meta-data associated with the trait named {alias}


   .. method:: pyre_registered(self)


      Hook that gets invoked by the framework after the component instance has been
      registered but before any configuration events


   .. method:: pyre_configured(self)


      Hook that gets invoked by the framework after the component instance has been
      configured but before the binding of any of its traits


   .. method:: pyre_initialized(self)


      Hook that gets invoked by the framework right before the component is put into
      action. The component is now in a known good state, with all configurable traits fully
      bound and validated. This is the place where the component should acquire whatever
      further resources it requires.


   .. method:: pyre_finalized(self)


      Hook that gets invoked by the framework right before the component is decommissioned.
      The instance should release all acquired resources.


   .. method:: pyre_getExtent(cls)
      :classmethod:


      Return the extent of this class, i.e. the set of its instances


   .. method:: pyre_slot(self, attribute=None)


      Return the slot associated with {attribute}; if no attribute s given, return the slot with
      the component instance itself


   .. method:: pyre_how(self, attribute)


      Return the priority associated with {attribute}


   .. method:: pyre_where(self, attribute=None)


      Return the locator associated with {attribute}; if no attribute name is given, return
      the locator of the component instance


   .. method:: pyre_classWhere(cls, attribute=None)
      :classmethod:


      Return the component class locator


   .. method:: __str__(self)



   .. method:: __getattr__(self, name)


      Trap attribute lookup errors and attempt to resolve the name in my inventory's name
      map. This makes it possible to get the value of a trait by using any of its aliases.


   .. method:: __setattr__(self, name, value)


      Trap attribute assignment and attempt to normalize the name before making the assignment


   .. method:: pyre_isCompatible(cls, spec, fast=True)
      :classmethod:


      Check whether {cls} is assignment compatible with {spec}, i.e. whether it provides at
      least the properties and behaviors specified by {spec}



