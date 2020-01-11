:mod:`pyre.platforms`
=====================

.. py:module:: pyre.platforms


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Bare/index.rst
   CPUInfo/index.rst
   CentOS/index.rst
   DPkg/index.rst
   Darwin/index.rst
   Debian/index.rst
   Host/index.rst
   Linux/index.rst
   MacPorts/index.rst
   Managed/index.rst
   Modules/index.rst
   POSIX/index.rst
   PackageManager/index.rst
   Platform/index.rst
   RedHat/index.rst
   Ubuntu/index.rst


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



.. py:class:: platform

   Bases: :class:`pyre.protocol`

   Encapsulation of host specific information

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      Build the preferred host implementation



.. py:class:: packager

   Bases: :class:`pyre.protocol`

   Encapsulation of host specific information

   .. method:: prefix(self)


      The package manager install location


   .. method:: installed(self)


      Retrieve available information for all installed packages


   .. method:: packages(self, category)


      Provide a sequence of package names that provide compatible installations for the given
      package {category}. If the package manager provides a way for the user to select a
      specific installation as the default, care should be taken to rank the sequence
      appropriately.


   .. method:: info(self, package)


      Return information about the given {package}

      The type of information returned is determined by the package manager. This method
      should return success if and only if {package} is actually fully installed.


   .. method:: contents(self, package)


      Generate a sequence of the contents of {package}

      The type of information returned is determined by the package manager. Typically, it
      contains the list of files that are installed by this package, but it may contain other
      filesystem entities as well. This method should return a non-empty sequence if and only
      if {pakage} is actually fully installed


   .. method:: configure(self, packageInstance)


      Dispatch to the {packageInstance} configuration procedure that is specific to the
      particular implementation of this protocol


   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      Build the preferred host implementation



.. function:: dpkg()

   Support for the Debian packager


.. function:: macports()

   Support for macports


.. function:: darwin()

   Support for OSX


.. function:: linux()

   Generic support for linux flavors


.. function:: centos()

   Support for CentOS


.. function:: redhat()

   Support for RedHat


.. function:: ubuntu()

   Support for Ubuntu


.. data:: osx
   

   

