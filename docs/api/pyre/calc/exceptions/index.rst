:mod:`pyre.calc.exceptions`
===========================

.. py:module:: pyre.calc.exceptions

.. autoapi-nested-parse::

   Definitions for all the exceptions raised by this package



Module Contents
---------------

.. py:exception:: EvaluationError(error, node=None, **kwds)

   Bases: :class:`pyre.algebraic.exceptions.NodeError`

   Base class for node evaluation exceptions

   .. attribute:: description
      :annotation: = evaluation error: {0.error}

      


.. py:exception:: ExpressionError

   Bases: :class:`pyre.algebraic.exceptions.NodeError`

   Base class for expression errors; useful when trapping them as a category


.. py:exception:: EmptyExpressionError(formula, **kwds)

   Bases: :class:`pyre.calc.exceptions.ExpressionError`

   Exception raised when the expression factory did not encounter any named references to
   other nodes

   .. attribute:: description
      :annotation: = while parsing {0.expression!r}: no references found

      


.. py:exception:: ExpressionSyntaxError(formula, error, **kwds)

   Bases: :class:`pyre.calc.exceptions.ExpressionError`

   Exception raised when the python interpreter encounters a syntax error while compiling the
   expression

   .. attribute:: description
      :annotation: = while evaluating {0.expression!r}: {0.error}

      


.. py:exception:: UnresolvedNodeError(name, node=None, **kwds)

   Bases: :class:`pyre.algebraic.exceptions.NodeError`

   Signal a value request from an unresolved node

   .. attribute:: description
      :annotation: = node {0.name!r} is unresolved

      


.. py:exception:: AliasingError(key, target, alias, targetNode, targetInfo, aliasNode, aliasInfo, **kwds)

   Bases: :class:`pyre.algebraic.exceptions.NodeError`

   Signal that an alias was requested among names that were associated with existing nodes

   .. attribute:: description
      :annotation: = both {0.target!r} and {0.alias!r} have existing nodes

      


