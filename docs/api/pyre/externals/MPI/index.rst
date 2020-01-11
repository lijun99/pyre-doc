:mod:`pyre.externals.MPI`
=========================

.. py:module:: pyre.externals.MPI


Module Contents
---------------

.. py:class:: MPI

   Bases: :class:`pyre.externals.Tool.Tool`, :class:`pyre.externals.Library.Library`

   The package manager for MPI packages

   .. attribute:: category
      :annotation: = mpi

      

   .. attribute:: launcher
      

      

   .. attribute:: doc
      :annotation: = the name of the launcher of MPI jobs

      

   .. method:: dpkgAlternatives(cls, dpkg)
      :classmethod:


      Identify the default implementation of MPI on dpkg machines


   .. method:: dpkgPackages(cls, packager)
      :classmethod:


      Provide alternative compatible implementations of python on dpkg machines, starting
      with the package the user has selected as the default


   .. method:: macportsPackages(cls, packager)
      :classmethod:


      Provide alternative compatible implementations of MPI on macports machines, starting with
      the package the user has selected as the default



.. py:class:: Default

   Bases: :class:`pyre.externals.ToolInstallation.ToolInstallation`, :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   The package manager for unknown MPI installations

   .. attribute:: flavor
      :annotation: = unknown

      

   .. attribute:: category
      

      

   .. attribute:: libraries
      

      

   .. attribute:: doc
      :annotation: = the libraries to place on the link line

      

   .. attribute:: launcher
      

      

   .. attribute:: doc
      :annotation: = the name of the launcher of MPI jobs

      

   .. method:: macports(self, packager)


      Attempt to repair my configuration



.. py:class:: OpenMPI

   Bases: :class:`pyre.externals.MPI.Default`

   The package manager for OpenMPI packages

   .. attribute:: flavor
      :annotation: = openmpi

      

   .. attribute:: category
      

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration



.. py:class:: MPICH

   Bases: :class:`pyre.externals.MPI.Default`

   The package manager for MPICH packages

   .. attribute:: flavor
      :annotation: = mpich

      

   .. attribute:: category
      

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration



