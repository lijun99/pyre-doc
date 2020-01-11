:mod:`pyre.externals.BLAS`
==========================

.. py:module:: pyre.externals.BLAS


Module Contents
---------------

.. py:class:: BLAS

   Bases: :class:`pyre.externals.Library.Library`

   The package manager for BLAS packages

   .. attribute:: category
      :annotation: = blas

      

   .. method:: dpkgAlternatives(cls, dpkg)
      :classmethod:


      Go through the installed packages and identify those that are relevant for providing
      support for my installations


   .. method:: dpkgPackages(cls, packager)
      :classmethod:


      Identify the default implementation of BLAS on dpkg machines


   .. method:: macportsPackages(cls, packager)
      :classmethod:


      Identify the default implementation of BLAS on macports machines



.. py:class:: Default

   Bases: :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   A generic BLAS installation

   .. attribute:: flavor
      :annotation: = unknown

      

   .. attribute:: category
      

      

   .. attribute:: libraries
      

      

   .. attribute:: doc
      :annotation: = the libraries to place on the link line

      


.. py:class:: Atlas

   Bases: :class:`pyre.externals.BLAS.Default`

   Atlas BLAS support

   .. attribute:: flavor
      :annotation: = atlas

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration


   .. method:: macports(self, packager)


      Attempt to repair my configuration



.. py:class:: OpenBLAS

   Bases: :class:`pyre.externals.BLAS.Default`

   OpenBLAS support

   .. attribute:: flavor
      :annotation: = openblas

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration


   .. method:: macports(self, packager)


      Attempt to repair my configuration



.. py:class:: GSLCBLAS

   Bases: :class:`pyre.externals.BLAS.Default`

   GSL BLAS support

   .. attribute:: flavor
      :annotation: = gslcblas

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration


   .. method:: macports(self, packager)


      Attempt to repair my configuration



