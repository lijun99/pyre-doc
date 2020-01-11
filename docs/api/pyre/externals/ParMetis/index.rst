:mod:`pyre.externals.ParMetis`
==============================

.. py:module:: pyre.externals.ParMetis


Module Contents
---------------

.. py:class:: ParMetis

   Bases: :class:`pyre.externals.Library.Library`

   The package manager for ParMetis packages

   .. attribute:: category
      :annotation: = parmetis

      

   .. method:: dpkgAlternatives(cls, dpkg)
      :classmethod:


      Go through the installed packages and identify those that are relevant for providing
      support for my installations


   .. method:: dpkgPackages(cls, packager)
      :classmethod:


      Identify the default implementation of ParMetis on dpkg machines


   .. method:: macportsPackages(cls, packager)
      :classmethod:


      Identify the default implementation of ParMetis on macports machines



.. py:class:: Default

   Bases: :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   A generic ParMetis installation

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



