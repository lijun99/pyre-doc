:mod:`pyre.components.exceptions`
=================================

.. py:module:: pyre.components.exceptions

.. autoapi-nested-parse::

   Definitions for all the exceptions raised by this package



Module Contents
---------------

.. py:exception:: ComponentError

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Base class for component specification errors


.. py:exception:: CategoryMismatchError(configurable, target, name, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when two configurables have traits by the same name but have different
   categories

   .. attribute:: description
      :annotation: = category mismatch in trait {0.name!r} between {0.configurable} and {0.target}

      


.. py:exception:: ImplementationSpecificationError(name, errors, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when the {implements} specification of a component declaration contains
   errors, e.g. classes that don't derive from Protocol

   .. attribute:: description
      :annotation: = {0.name}: poorly formed implementation specification

      


.. py:exception:: ProtocolError(component, protocol, report, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when a component does not implement correctly the protocols in its
   implementation specification


.. py:exception:: TraitNotFoundError(configurable, name, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when a request for a trait fails

   .. attribute:: description
      :annotation: = {0.configurable} has no trait named {0.name!r}

      


.. py:exception:: FacilitySpecificationError(configurable, trait, value, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when a facility cannot instantiate its configuration specification

   .. attribute:: description
      :annotation: = {0.__name__}.{0.trait.name}: could not instantiate {0.value!r}

      


.. py:exception:: ProtocolCompatibilityError(configurable, protocol, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when a configurable is incompatible with a suggested protocol

   .. attribute:: description
      :annotation: = {0.configurable} is incompatible with {0.protocol}

      


.. py:exception:: ResolutionError(protocol, value, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when a protocol cannot resolve a string into a component

   .. attribute:: description
      :annotation: = could not resolve {0.value!r} into a component that implements {0.protocol}

      


.. py:exception:: DefaultError(protocol, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when a protocol cannot determine a valid default value

   .. attribute:: description
      :annotation: = no valid default binding for {0.protocol}

      


.. py:exception:: ConfigurationError(configurable, errors, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when something bad happens during component configuration

   .. attribute:: description
      :annotation: = while configuring {0.configurable}:
       {0.report}

      

   .. method:: report(self)
      :property:


      Splice my errors together



.. py:exception:: InitializationError(configurable, errors, **kwds)

   Bases: :class:`pyre.components.exceptions.ComponentError`

   Exception raised when something bad happens during component initialization

   .. attribute:: description
      :annotation: = while initializing {0.configurable}:
       {0.report}

      

   .. method:: report(self)
      :property:


      Splice my errors together



