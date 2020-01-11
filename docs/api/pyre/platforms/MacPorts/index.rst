:mod:`pyre.platforms.MacPorts`
==============================

.. py:module:: pyre.platforms.MacPorts


Module Contents
---------------

.. py:class:: MacPorts(**kwds)

   Bases: :class:`pyre.platforms.Managed.Managed`

   Support for the macport package manager

   .. attribute:: name
      :annotation: = macports

      

   .. attribute:: client
      :annotation: = port

      

   .. attribute:: defaultLocation
      

      

   .. attribute:: _installed
      

      

   .. attribute:: _alternatives
      

      

   .. attribute:: _normalizations
      

      

   .. attribute:: _provides
      

      

   .. method:: getInstalledPackages(self)


      Grant access to the installed package indexx


   .. method:: alternatives(self, group)


      Generate a sequence of alternative installations for {group}, starting with the default
      selection


   .. method:: getAlternatives(self)


      Return the selected package and all alternatives for the given package {group}


   .. method:: retrieveInstalledPackages(self)


      Ask macports for installed package information


   .. method:: retrievePackageContents(self, package)


      Generate a sequence with the contents of {package}


   .. method:: retrievePackageAlternatives(self)


      Retrieve selection information for all known package groups


   .. method:: getSelectionInfo(self, group, alternative)


      Identify the package in the {group} that provides the selected {alternative}


   .. method:: getNormalization(self, group, alternative)


      Retrieve the normalization map for {alternative} from {group}


   .. method:: retrieveNormalizationTable(self, group, alternative)


      Populate the {group} normalization table with the selections for {alternative}


   .. method:: getFileProvider(self, filename)


      Find the package that owns the given filename


   .. method:: identify(self, installation)


      Attempt to map the package {installation} to the name of an installed package



