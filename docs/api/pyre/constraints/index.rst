:mod:`pyre.constraints`
=======================

.. py:module:: pyre.constraints

.. autoapi-nested-parse::

   This package provides access to the set of builtin constraints.

   Constraints are predicates that raise a ConstraintViolationError exception whenever the value
   they were asked to validate fails to meet their specific criteria. They are frequently used to
   validate trait values supplied by the end-user.

   The factories in this package build constraint instances out of the given input parameters that
   specify a constraint. These instances can be later used to verify that values satisfy them by
   calling the method validate of the constraint, or more simply, by using the constraint itself
   as a function.

   For example:

       import pyre.constraints
       g = pyre.constraints.isGreater(value=0)
       # check that the value 10 satisfies it
       g.validate(10)
       # or, equivalently
       g(10)

   is one way you could implement the constraint "check that value is a positive number" and use
   it to check that 10 does indeed statisfy it.

   Instead of being functions that return booleans, constraints throw exceptions when they are
   violated. This design choice is motivated by the observation that it is not always possible to
   handle a constraint violation locally, since the caller may not have enough information to
   handle the failure.



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   And/index.rst
   Between/index.rst
   Comparison/index.rst
   Constraint/index.rst
   Equal/index.rst
   Greater/index.rst
   GreaterEqual/index.rst
   Less/index.rst
   LessEqual/index.rst
   Like/index.rst
   Not/index.rst
   Or/index.rst
   Set/index.rst
   Subset/index.rst
   exceptions/index.rst


Package Contents
----------------

.. function:: isAll(*constraints)

   Passes when all the constraints in its list pass


.. function:: isAny(*constraints)

   Passes when any of the constraints in its list passes


.. function:: isBetween(*, low, high)

   Check that a numeric value is between {low} and {high}


.. function:: isEqual(*, value)

   Check that a numeric value is equal to {value}


.. function:: isGreater(*, value)

   Check that a numeric value is greater than {value}


.. function:: isGreaterEqual(*, value)

   Check that a numeric value is greater or equal to {value}


.. function:: isLess(*, value)

   Check that a numeric value is less than {value}


.. function:: isLessEqual(*, value)

   Check that a numeric value is less than or equal to {value}


.. function:: isLike(*, regexp)

   Check that the value matches {regexp}, where {regexp} is a re-style regular expression. See
   the re builtin module


.. function:: isMember(*choices)

   Check that the value supplied is one of {choices}


.. function:: isNegative()

   Check that the given value is less than zero


.. function:: isNot(constraint)

   Check that value makes {constraint} fail


.. function:: isPositive()

   Check that the given value is greater than or equal to zero


.. function:: isSubset(*, choices)

   Check that the given set is a subset of {choices}


