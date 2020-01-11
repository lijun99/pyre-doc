:mod:`pyre.externals.GCC`
=========================

.. py:module:: pyre.externals.GCC


Module Contents
---------------

.. py:class:: GCC

   Bases: :class:`pyre.externals.Tool.Tool`

   The package manager for GCC installations

   .. attribute:: category
      :annotation: = gcc

      

   .. attribute:: wrapper
      

      

   .. attribute:: doc
      :annotation: = the name of the compiler front end

      

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


      Identify the default implementation of GCC on macports machines



.. py:class:: Default

   Bases: :class:`pyre.externals.ToolInstallation.ToolInstallation`

   Support for GCC installations

   .. attribute:: category
      

      

   .. attribute:: flavor
      

      

   .. attribute:: wrapper
      

      

   .. attribute:: doc
      :annotation: = the name of the compiler front end

      

   .. attribute:: _versionRegex
      

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration


   .. method:: macports(self, packager)


      Attempt to repair my configuration


   .. method:: retrieveVersion(self)


      Get my version number directly from the compiler

      In general, this is not needed except on hosts with no package managers to help me



.. py:class:: GCC4

   Bases: :class:`pyre.externals.GCC.Default`

   Support for GCC 4.x installations

   .. attribute:: flavor
      

      


.. py:class:: GCC5

   Bases: :class:`pyre.externals.GCC.Default`

   Support for GCC 5.x installations

   .. attribute:: flavor
      

      


.. py:class:: CLang(**kwds)

   Bases: :class:`pyre.externals.ToolInstallation.ToolInstallation`

   Apple's clang

   .. attribute:: category
      

      

   .. attribute:: wrapper
      

      

   .. attribute:: doc
      :annotation: = the name of the compiler front end

      

   .. attribute:: _versionRegex
      

      

   .. method:: retrieveVersion(self)


      Get my version number



