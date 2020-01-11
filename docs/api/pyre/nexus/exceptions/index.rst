:mod:`pyre.nexus.exceptions`
============================

.. py:module:: pyre.nexus.exceptions


Module Contents
---------------

.. py:exception:: NexusError

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Base exceptions for all error conditions detected by nexus components


.. py:exception:: RecoverableError

   Bases: :class:`pyre.nexus.exceptions.NexusError`

   A recoverable error has occurred


.. py:exception:: ConnectionResetError

   Bases: :class:`pyre.nexus.exceptions.NexusError`

   The connection was closed by the peer


