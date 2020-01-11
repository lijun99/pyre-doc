:mod:`pyre.externals.Python`
============================

.. py:module:: pyre.externals.Python


Module Contents
---------------

.. py:class:: Python

   Bases: :class:`pyre.externals.Tool.Tool`, :class:`pyre.externals.Library.Library`

   The package manager for the python interpreter

   .. attribute:: category
      :annotation: = python

      

   .. attribute:: interpreter
      

      

   .. attribute:: doc
      :annotation: = the full path to the interpreter

      

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


      Provide alternative compatible implementations of python on macports machines, starting
      with the package the user has selected as the default



.. py:class:: Default

   Bases: :class:`pyre.externals.ToolInstallation.ToolInstallation`, :class:`pyre.externals.LibraryInstallation.LibraryInstallation`

   The base class for for python instances

   .. attribute:: flavor
      

      

   .. attribute:: category
      

      

   .. attribute:: libraries
      

      

   .. attribute:: doc
      :annotation: = the libraries to place on the link line

      

   .. attribute:: interpreter
      

      

   .. attribute:: doc
      :annotation: = the full path to the python interpreter

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration


   .. method:: macports(self, packager)


      Attempt to repair my configuration



.. py:class:: Python2

   Bases: :class:`pyre.externals.Python.Default`

   The package manager for python 2.x instances

   .. attribute:: flavor
      

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      


.. py:class:: Python3

   Bases: :class:`pyre.externals.Python.Default`

   The package manager for python 3.x instances

   .. attribute:: flavor
      

      

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      


