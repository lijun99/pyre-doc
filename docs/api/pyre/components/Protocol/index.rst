:mod:`pyre.components.Protocol`
===============================

.. py:module:: pyre.components.Protocol


Module Contents
---------------

.. py:class:: Protocol

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



