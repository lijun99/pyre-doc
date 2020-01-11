:mod:`pyre.constraints.exceptions`
==================================

.. py:module:: pyre.constraints.exceptions

.. autoapi-nested-parse::

   Definitions for all the exceptions raised by this package



Module Contents
---------------

.. py:exception:: ConstraintViolationError(constraint, value, **kwds)

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Exception used to indicate that a constraint is violated

   Instead of being functions that return booleans, constraints throw exceptions when they are
   violated. This design choice is motivated by the observation that it is not always possible
   to handle a constraint violation locally, since the caller may not have enough information
   to handle the failure.

   .. attribute:: description
      :annotation: = {0.value!r} is not {0.constraint}

      


