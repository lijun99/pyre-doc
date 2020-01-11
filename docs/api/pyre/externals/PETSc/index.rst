:mod:`pyre.externals.PETSc`
===========================

.. py:module:: pyre.externals.PETSc


Module Contents
---------------

.. py:class:: PETSc

   Bases: :class:`pyre.externals.Library.Library`

   The package manager for PETSc packages

   .. attribute:: category
      :annotation: = petsc

      

   .. method:: dpkgAlternatives(cls, dpkg)
      :classmethod:


      Go through the installed packages and identify those that are relevant for providing
      support for my installations


   .. method:: dpkgPackages(cls, packager)
      :classmethod:


      Identify the default implementation of PETSc on dpkg machines


   .. method:: macportsPackages(cls, packager)
      :classmethod:


      Identify the default implementation of PETSc on macports machines



.. py:class:: Default

   Bases: :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   A generic PETSc installation

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



