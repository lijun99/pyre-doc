:mod:`pyre`
===========

.. py:module:: pyre

.. autoapi-nested-parse::

   pyre is a framework for building flexible applications

   For more details, see http://pyre.orthologue.com.
   For terms of use, see pyre.license()



Subpackages
-----------
.. toctree::
   :titlesonly:
   :maxdepth: 3

   algebraic/index.rst
   calc/index.rst
   components/index.rst
   config/index.rst
   constraints/index.rst
   db/index.rst
   descriptors/index.rst
   extensions/index.rst
   externals/index.rst
   filesystem/index.rst
   flow/index.rst
   framework/index.rst
   geometry/index.rst
   grid/index.rst
   handbook/index.rst
   http/index.rst
   ipc/index.rst
   nexus/index.rst
   parsing/index.rst
   patterns/index.rst
   platforms/index.rst
   primitives/index.rst
   records/index.rst
   schemata/index.rst
   shells/index.rst
   tabular/index.rst
   timers/index.rst
   tracking/index.rst
   traits/index.rst
   units/index.rst
   weaver/index.rst
   xml/index.rst


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   meta/index.rst
   services/index.rst


Package Contents
----------------

.. function:: resolve(uri)

   Interpret {uri} as a request to locate and load a component


.. function:: loadConfiguration(uri)

   Open {uri} and attempt to load its contents into the configaration model


.. function:: computeCallerStackDepth()

   Compute the stack depth offset to get to the caller of a function


.. function:: copyright()

   Return the pyre copyright note


.. function:: license()

   Print the pyre license


.. function:: version()

   Return the pyre version


.. function:: credits()

   Print the acknowledgments


.. function:: where(configurable, attribute=None)

   Retrieve the location where the {attribute} of {configurable} got its value; if no
   {attribute} is specified, retrieve information about the {configurable} itself


.. function:: boot()

   Perform all the initialization steps necessary to bootstrap the framework


.. function:: debug()

   Enable debugging of pyre modules.

   Modules that support debugging must provide a {debug} method and do as little as possible
   during their initialization. The fundamental constraints are provided by the python import
   algorithm that only give you one chance to import a module.

   This must be done very early, before pyre itself starts importing its packages. One way to
   request debugging is to create a variable {pyre_debug} in the __main__ module that contains
   a set of strings, each one of which is the name of a pyre module that you would like to
   debug.


.. py:class:: actor(name, bases, attributes, *, family=None, **kwds)

   Bases: :class:`pyre.components.Requirement.Requirement`

   The metaclass of components

   {Actor} takes care of all the tasks necessary to convert a component declaration into a
   configurable entity that coöperates fully with the framework

   .. method:: pyre_name(self)
      :property:


      Return the component's family name


   .. method:: __call__(self, name=None, locator=None, globalAliases=False, **kwds)


      Build an instance of one of my classes


   .. method:: __setattr__(self, name, value)


      Trap attribute setting in my class record instances to support setting the default
      value using the natural syntax


   .. method:: __str__(self)



   .. method:: pyre_buildProtocol(cls, name, bases, implements)
      :classmethod:


      Build a class that describes the implementation requirements imposed on this
      {component}, given its class record and the list of protocols it {implements}



.. py:class:: role(name, bases, attributes, *, family=None, **kwds)

   Bases: :class:`pyre.components.Requirement.Requirement`

   The metaclass for protocols

   .. method:: pyre_name(self)
      :property:


      The protocol's name is its family name


   .. method:: __call__(self, **kwds)


      The instantiation of protocol objects creates facility descriptors


   .. method:: __str__(self)



   .. method:: facility(self, **kwds)


      Build my trait descriptor



.. py:class:: protocol

   Bases: :class:`pyre.components.Configurable.Configurable`

   The base class for requirement specifications

   .. attribute:: pyre_key
      

      

   .. attribute:: pyre_isProtocol
      :annotation: = True

      

   .. attribute:: EXTENSION
      :annotation: = .py

      

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The preferred implementation of this protocol, in case the user has not provided an
      alternative


   .. method:: pyre_convert(cls, value, **kwds)
      :classmethod:


      Hook to enable protocols to translate the component specification in {value} into a
      canonical form


   .. method:: pyre_family(cls)
      :classmethod:


      Look up my family name


   .. method:: pyre_familyFragments(cls)
      :classmethod:


      Look up my family name


   .. method:: pyre_package(cls)
      :classmethod:


      Deduce my package name


   .. method:: pyre_public(cls)
      :classmethod:


      Generate the sequence of my public ancestors, i.e. the ones that have a non-trivial family


   .. method:: pyre_resolveSpecification(cls, spec, **kwds)
      :classmethod:


      Attempt to resolve {spec} into a component that implements me; {spec} is
      assumed to be a string


   .. method:: pyre_resolutionContext(cls)
      :classmethod:


      Return an iterable over portions of my family name


   .. method:: pyre_locateAllImplementers(cls)
      :classmethod:


      Retrieve all visible components that are compatible with me

      For components to be visible, their location has to be deducible based only on the
      information available to this protocol; other compatible components may be provided by
      packages that have not been imported yet, or live in files outside the canonical layout


   .. method:: pyre_locateAllRegisteredImplementers(cls)
      :classmethod:


      Retrieve all implementers that are already registered with the framework

      This catches components whose source has been seen by the framework at the time this
      method was invoked; the information available may be different during a subsequent call
      if pyre has bumped into additional implementers


   .. method:: pyre_locateAllImportableImplementers(cls)
      :classmethod:


      Retrieve all implementers registered in a namespace derivable from my family name


   .. method:: pyre_locateAllLoadableImplementers(cls)
      :classmethod:


      Retrieve all implementers that live in files and folders derivable from my family name


   .. method:: pyre_implementers(cls, uri)
      :classmethod:


      Retrieve components that are compatible with me from the shelf in {uri}


   .. method:: pyre_isCompatible(cls, spec, fast=True)
      :classmethod:


      Check whether {this} protocol is compatible with the {other}


   .. method:: pyre_isTypeCompatible(cls, protocol)
      :classmethod:


      Decide whether {cls} is type compatible with the given {protocol}

      The intent here is to enable protocols to tighten or loosen this definition to fit
      their specific use cases. The implementation is based on pedigree comparisons between
      {cls} and {protocol}



.. py:class:: component(name, locator, **kwds)

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



.. py:class:: foundry(factory, implements=None, tip='', **kwds)

   A decorator for callables that return component classes

   .. attribute:: pyre_tip
      :annotation: = 

      

   .. attribute:: pyre_factory
      

      

   .. attribute:: pyre_implements
      

      

   .. method:: __call__(self, *args, **kwds)



   .. method:: sequify(self, items)
      :classmethod:


      Normalize {items} into a tuple



.. py:class:: monitor

   Bases: :class:`pyre.calc.Probe.Probe`

   A probe that monitors the traits of a set of components

   .. method:: watch(self, component)


      Monitor {component} for changes in the values of its traits



.. py:class:: tracker(**kwds)

   Bases: :class:`pyre.components.Monitor.Monitor`

   A class that monitors the traits of a set of components and maintains a record of their values

   .. method:: track(self, component)


      Add the {component} traits to the pile of observables


   .. method:: flush(self, observable, **kwds)


      Handle the notification that the value of {observable} has changed



.. data:: property
   

   

.. py:class:: export(method, tip=None, **kwds)

   Bases: :class:`pyre.traits.Trait.Trait`

   The base class for component methods that are part of its external interface

   .. attribute:: method
      

      

   .. attribute:: category
      :annotation: = behavior

      

   .. attribute:: isBehavior
      :annotation: = True

      

   .. method:: __get__(self, instance, cls)


      Access to the behavior


   .. method:: __set__(self, instance, value)


      Disable writing to behavior descriptors


   .. method:: __str__(self)




.. py:class:: provides(method, tip=None, **kwds)

   Bases: :class:`pyre.traits.Trait.Trait`

   The base class for component methods that are part of its external interface

   .. attribute:: method
      

      

   .. attribute:: category
      :annotation: = behavior

      

   .. attribute:: isBehavior
      :annotation: = True

      

   .. method:: __get__(self, instance, cls)


      Access to the behavior


   .. method:: __set__(self, instance, value)


      Disable writing to behavior descriptors


   .. method:: __str__(self)




.. py:class:: facility(protocol, **kwds)

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




.. py:exception:: PyreError(description=None, locator=None, **kwds)

   Bases: :class:`Exception`

   Base class for all pyre related errors

   .. attribute:: description
      :annotation: = generic pyre error

      

   .. method:: __str__(self)




.. data:: executive
   

   

.. data:: package
   

   

.. function:: shutdown()

   Attempt to hunt down and destroy all known references to the executive


