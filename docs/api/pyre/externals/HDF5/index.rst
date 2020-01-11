:mod:`pyre.externals.HDF5`
==========================

.. py:module:: pyre.externals.HDF5


Module Contents
---------------

.. py:class:: HDF5

   Bases: :class:`pyre.externals.Library.Library`

   The package manager for HDF5 packages

   .. attribute:: category
      :annotation: = hdf5

      

   .. method:: dpkgAlternatives(cls, dpkg)
      :classmethod:


      Go through the installed packages and identify those that are relevant for providing
      support for my installations


   .. method:: dpkgPackages(cls, packager)
      :classmethod:


      Identify the default implementation of HDF5 on dpkg machines


   .. method:: macportsPackages(cls, packager)
      :classmethod:


      Identify the default implementation of HDF5 on macports machines



.. py:class:: Default

   Bases: :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   A generic HDF5 installation

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



