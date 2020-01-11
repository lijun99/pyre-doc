:mod:`merlin.components.exceptions`
===================================

.. py:module:: merlin.components.exceptions


Module Contents
---------------

.. py:exception:: MerlinError

   Bases: :class:`pyre.PyreError`

   Base class for merlin exceptions


.. py:exception:: SpellNotFoundError(spell, **kwds)

   Bases: :class:`merlin.components.exceptions.MerlinError`

   Exception raised when the requested spell cannot be located

   .. attribute:: description
      :annotation: = spell {.spell!r} not found

      


