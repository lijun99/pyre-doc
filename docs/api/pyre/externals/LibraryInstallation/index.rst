:mod:`pyre.externals.LibraryInstallation`
=========================================

.. py:module:: pyre.externals.LibraryInstallation


Module Contents
---------------

.. py:class:: LibraryInstallation

   Bases: :class:`pyre.externals.Installation.Installation`

   The package manager for libraries

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. attribute:: incdir
      

      

   .. attribute:: doc
      :annotation: = the locations of my headers; for the compiler command line

      

   .. attribute:: libdir
      

      

   .. attribute:: doc
      :annotation: = the locations of my libraries; for the linker command path

      

   .. method:: pyre_configured(self)


      Verify that my {incdir} and {libdir} traits point to good locations



