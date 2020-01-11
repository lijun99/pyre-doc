:mod:`pyre.components.Configurable`
===================================

.. py:module:: pyre.components.Configurable


Module Contents
---------------

.. py:class:: Configurable

   Bases: :class:`pyre.framework.Dashboard.Dashboard`

   The base class for components and interfaces

   This class provides storage for class attributes and a place to park utilities that are
   common to both components and interfaces

   .. attribute:: pyre_pedigree
      

      

   .. attribute:: pyre_localTraits
      :annotation: = []

      

   .. attribute:: pyre_inheritedTraits
      :annotation: = []

      

   .. attribute:: pyre_namemap
      

      

   .. attribute:: pyre_traitmap
      

      

   .. attribute:: pyre_locator
      

      

   .. attribute:: pyre_internal
      :annotation: = True

      

   .. attribute:: pyre_isProtocol
      :annotation: = False

      

   .. attribute:: pyre_isComponent
      :annotation: = False

      

   .. method:: pyre_help(self, indent=' ' * 4, **kwds)


      Hook for the application help system


   .. method:: pyre_showConfiguration(self, indent='', deep=False)


      Traverse my configuration tree and display trait metadata


   .. method:: pyre_renderConfiguration(self, deep=True)


      Traverse my configuration and represent it in a JSON friendly way


   .. method:: pyre_showSummary(self, indent, **kwds)


      Generate a short description of what I do


   .. method:: pyre_showConfigurables(self, indent='', **kwds)


      Generate a description of my configurable state


   .. method:: pyre_showBehaviors(self, spec, indent, **kwds)


      Generate a description of my interface


   .. method:: pyre_traits(cls)
      :classmethod:


      Generate a sequence of all my trait descriptors, both locally declared and inherited.
      If you are looking for the traits declared in a particular class, use the attribute
      {cls.pyre_localTraits} instead.


   .. method:: pyre_configurables(cls)
      :classmethod:


      Generate a sequence of all my trait descriptors that are marked as configurable.


   .. method:: pyre_behaviors(cls)
      :classmethod:


      Generate a sequence of all my trait descriptors that are marked as configurable.


   .. method:: pyre_properties(cls)
      :classmethod:


      Generate a sequence of all my trait descriptors that are marked as properties


   .. method:: pyre_facilities(cls)
      :classmethod:


      Generate a sequence of all my trait descriptors that are marked as facilities


   .. method:: pyre_localConfigurables(cls)
      :classmethod:


      Generate a sequence of my local trait descriptors that are marked as configurable.


   .. method:: pyre_localBehaviors(cls)
      :classmethod:


      Generate a sequence of my local trait descriptors that are marked as behaviors


   .. method:: pyre_localProperties(cls)
      :classmethod:


      Generate a sequence of my local trait descriptors that are marked as properties


   .. method:: pyre_localFacilities(cls)
      :classmethod:


      Generate a sequence of all my trait descriptors that are marked as facilities


   .. method:: pyre_trait(cls, alias)
      :classmethod:


      Given the name {alias}, locate and return the associated descriptor


   .. method:: pyre_classRegistered(cls)
      :classmethod:


      Hook that gets invoked by the framework after the class record has been registered but
      before any configuration events


   .. method:: pyre_classConfigured(cls)
      :classmethod:


      Hook that gets invoked by the framework after the class record has been configured,
      before any instances have been created


   .. method:: pyre_classInitialized(cls)
      :classmethod:


      Hook that gets invoked by the framework after the class record has been initialized,
      before any instances have been created


   .. method:: pyre_isCompatible(cls, spec, fast=True)
      :classmethod:


      Check whether {cls} is assignment compatible with {spec}

      Here, we confine ourselves to the part of the problem that involves assignment
      compatibility, i.e. whether {cls} provides at least the properties and behaviors
      specified by {spec}. More general compatibility notions are supported by the
      subclasses.

      If {fast} is True, this method will return as soon as it encounters the first
      incompatibility issue, without performing an exhaustive check of all traits. If {fast}
      is False, a thorough check of all traits will be performed resulting in a detailed
      compatibility report.



