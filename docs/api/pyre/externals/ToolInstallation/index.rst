:mod:`pyre.externals.ToolInstallation`
======================================

.. py:module:: pyre.externals.ToolInstallation


Module Contents
---------------

.. py:class:: ToolInstallation

   Bases: :class:`pyre.externals.Installation.Installation`

   The package manager for generic tools

   .. attribute:: bindir
      

      

   .. attribute:: doc
      :annotation: = the location of my binaries

      

   .. method:: binaries(self, **kwds)


      A sequence of names of binaries to look for


   .. method:: pyre_configured(self)


      Verify that the {bindir} trait points to a good location



