:mod:`pyre.externals.VTK`
=========================

.. py:module:: pyre.externals.VTK


Module Contents
---------------

.. py:class:: VTK

   Bases: :class:`pyre.externals.Library.Library`

   The package manager for VTK packages

   .. attribute:: category
      :annotation: = vtk

      

   .. method:: dpkgAlternatives(cls, dpkg)
      :classmethod:


      Go through the installed packages and identify those that are relevant for providing
      support for my installations


   .. method:: dpkgPackages(cls, packager)
      :classmethod:


      Identify the default implementation of HDF5 on dpkg machines


   .. method:: macportsPackages(cls, packager)
      :classmethod:


      Identify the default implementation of VTK on macports machines



.. py:class:: VTK5

   Bases: :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   Support for VTK 5.x installations

   .. attribute:: category
      

      

   .. attribute:: flavor
      

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. attribute:: libraries
      

      

   .. attribute:: doc
      :annotation: = the libraries to place on the link line

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration


   .. method:: macports(self, packager, **kwds)


      Attempt to repair my configuration



.. py:class:: VTK6

   Bases: :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   Support for VTK 6.x installations

   .. attribute:: category
      

      

   .. attribute:: flavor
      

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. attribute:: libraries
      

      

   .. attribute:: doc
      :annotation: = the libraries to place on the link line

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration


   .. method:: macports(self, packager, **kwds)


      Attempt to repair my configuration


   .. method:: libgen(self, stem)


      Construct the name of a library given a capability {stem}



