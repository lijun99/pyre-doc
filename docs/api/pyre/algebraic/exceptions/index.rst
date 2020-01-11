:mod:`pyre.algebraic.exceptions`
================================

.. py:module:: pyre.algebraic.exceptions

.. autoapi-nested-parse::

   Definitions for all the exceptions raised by this package



Module Contents
---------------

.. py:exception:: NodeError

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Base class for pyre.algebraic errors. Useful as a catch-all


.. py:exception:: CircularReferenceError(node, path=(), **kwds)

   Bases: :class:`pyre.algebraic.exceptions.NodeError`

   Signal a circular reference in the evaluation graph

   .. attribute:: description
      :annotation: = the evaluation graph has a cycle at {0.node}

      


