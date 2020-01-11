:mod:`pyre.platforms.PackageManager`
====================================

.. py:module:: pyre.platforms.PackageManager


Module Contents
---------------

.. py:class:: PackageManager

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



