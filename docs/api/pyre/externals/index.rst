:mod:`pyre.externals`
=====================

.. py:module:: pyre.externals


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   BLAS/index.rst
   Cython/index.rst
   GCC/index.rst
   GSL/index.rst
   HDF5/index.rst
   Installation/index.rst
   Library/index.rst
   LibraryInstallation/index.rst
   MPI/index.rst
   Metis/index.rst
   PETSc/index.rst
   Package/index.rst
   ParMetis/index.rst
   Postgres/index.rst
   Python/index.rst
   Tool/index.rst
   ToolInstallation/index.rst
   VTK/index.rst


Package Contents
----------------

.. py:class:: foundry(factory, implements=None, tip='', **kwds)

   A decorator for callables that return component classes

   .. attribute:: pyre_tip
      :annotation: = 

      

   .. attribute:: pyre_factory
      

      

   .. attribute:: pyre_implements
      

      

   .. method:: __call__(self, *args, **kwds)



   .. method:: sequify(self, items)
      :classmethod:


      Normalize {items} into a tuple



.. function:: catalog(**kwds)

   Build a trait descriptor suitable for building a database of available external packages
   for each package category


.. function:: dependencies(**kwds)

   Build a trait descriptor suitable for building a database of external package choices for
   each package category


.. function:: requirements(**kwds)

   Build a trait descriptor suitable for describing the list of package categories on which
   applications depend


.. py:class:: package

   Bases: :class:`pyre.protocol`

   The protocol that all external package managers must implement

   .. attribute:: version
      

      

   .. attribute:: doc
      :annotation: = the package version

      

   .. attribute:: prefix
      

      

   .. attribute:: doc
      :annotation: = the package installation directory

      

   .. attribute:: category
      

      

   .. method:: pyre_default(cls, channel=None, **kwds)
      :classmethod:


      Identify the default implementation of a package



.. py:class:: tool

   Bases: :class:`pyre.externals.Package.Package`

   Base class for external tools

   .. attribute:: bindir
      

      

   .. attribute:: doc
      :annotation: = the locations of my binaries

      


.. py:class:: library

   Bases: :class:`pyre.externals.Package.Package`

   Base class for third party libraries

   .. attribute:: defines
      

      

   .. attribute:: doc
      :annotation: = the compile time markers that indicate my presence

      

   .. attribute:: incdir
      

      

   .. attribute:: doc
      :annotation: = the locations of my headers; for the compiler command line

      

   .. attribute:: libdir
      

      

   .. attribute:: doc
      :annotation: = the locations of my libraries; for the linker command path

      


.. function:: blas()

   The BLAS package manager


.. function:: cython()

   The Cython package manager


.. function:: gcc()

   The GCC package manager


.. function:: gsl()

   The GSL package manager


.. function:: hdf5()

   The HDF5 package manager


.. function:: metis()

   The metis package manager


.. function:: mpi()

   The MPI package manager


.. function:: parmetis()

   The parmetis package manager


.. function:: petsc()

   The PETSc package manager


.. function:: postgres()

   The Postgres package manager


.. function:: python()

   The Python package manager


.. function:: vtk()

   The VTK package manager


