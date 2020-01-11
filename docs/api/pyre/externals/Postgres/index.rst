:mod:`pyre.externals.Postgres`
==============================

.. py:module:: pyre.externals.Postgres


Module Contents
---------------

.. py:class:: Postgres

   Bases: :class:`pyre.externals.Tool.Tool`, :class:`pyre.externals.Library.Library`

   The package manager for postgres client development

   .. attribute:: category
      :annotation: = postgresql

      

   .. attribute:: psql
      

      

   .. attribute:: doc
      :annotation: = the full path to the postgres client

      

   .. method:: dpkgAlternatives(cls, dpkg)
      :classmethod:


      Go through the installed packages and identify those that are relevant for providing
      support for my installations


   .. method:: dpkgPackages(cls, packager)
      :classmethod:


      Provide alternative compatible implementations of python on dpkg machines, starting
      with the package the user has selected as the default


   .. method:: macportsPackages(cls, packager)
      :classmethod:


      Identify the default implementation of postgres on macports machines



.. py:class:: Default

   Bases: :class:`pyre.externals.ToolInstallation.ToolInstallation`, :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   A generic postgres installation

   .. attribute:: category
      

      

   .. attribute:: flavor
      

      

   .. attribute:: psql
      

      

   .. attribute:: doc
      :annotation: = the full path to the postgres client

      

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



