:mod:`pyre.externals.Cython`
============================

.. py:module:: pyre.externals.Cython


Module Contents
---------------

.. py:class:: Cython

   Bases: :class:`pyre.externals.Tool.Tool`

   The package manager for the cython interpreter

   .. attribute:: category
      :annotation: = cython

      

   .. attribute:: compiler
      

      

   .. attribute:: doc
      :annotation: = the name of the compiler; may be the full path to the executable

      

   .. method:: dpkgAlternatives(cls, dpkg)
      :classmethod:


      Go through the installed packages and identify those that are relevant for providing
      support for my installations


   .. method:: dpkgPackages(cls, packager)
      :classmethod:


      Identify the default implementation of BLAS on dpkg machines


   .. method:: macportsPackages(cls, packager)
      :classmethod:


      Provide alternative compatible implementations of cython on macports machines, starting
      with the package the user has selected as the default



.. py:class:: Default

   Bases: :class:`pyre.externals.ToolInstallation.ToolInstallation`

   The package manager for cython instances

   .. attribute:: category
      

      

   .. attribute:: flavor
      

      

   .. attribute:: compiler
      

      

   .. attribute:: doc
      :annotation: = the name of the cython compiler

      

   .. method:: dpkg(self, packager)


      Attempt to repair my configuration


   .. method:: macports(self, packager)


      Attempt to repair my configuration



.. py:class:: Cython2

   Bases: :class:`pyre.externals.Cython.Default`

   The package manager for cython 2.x instances

   .. attribute:: flavor
      

      


.. py:class:: Cython3

   Bases: :class:`pyre.externals.Cython.Default`

   The package manager for cython 3.x instances

   .. attribute:: flavor
      

      


