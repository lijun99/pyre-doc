:mod:`pyre.platforms.DPkg`
==========================

.. py:module:: pyre.platforms.DPkg


Module Contents
---------------

.. py:class:: DPkg(**kwds)

   Bases: :class:`pyre.platforms.Managed.Managed`

   Support for the debian package manager

   .. attribute:: name
      :annotation: = dpkg

      

   .. attribute:: client
      :annotation: = dpkg-query

      

   .. attribute:: defaultLocation
      

      

   .. attribute:: _installed
      

      

   .. attribute:: _alternatives
      

      

   .. attribute:: _infoParser
      

      

   .. method:: alternatives(self, group)


      Generate a sequence of alternative installations for {group}, starting with the default
      selection


   .. method:: identify(self, installation)


      Attempt to map the package {installation} to the name of an installed package


   .. method:: setAlternatives(self, group, options)


      Attach the table of available {options} for the given package {group}

      The table of options is a map from the constructed pyre legal installation names to the
      names of the packages that support them


   .. method:: getInstalledPackages(self)


      Return the version and revision of all installed packages


   .. method:: retrieveInstalledPackages(self)


      Generate a sequence of all installed ports


   .. method:: retrievePackageContents(self, package)


      Generate a sequence of the contents of {package}



