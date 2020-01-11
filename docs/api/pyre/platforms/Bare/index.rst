:mod:`pyre.platforms.Bare`
==========================

.. py:module:: pyre.platforms.Bare


Module Contents
---------------

.. py:class:: Bare

   Bases: :class:`pyre.component`

   Support for un*x systems that don't have package management facilities

   .. attribute:: name
      :annotation: = bare

      

   .. method:: prefix(self)


      The package manager install location


   .. method:: installed(self)


      Retrieve available information for all installed packages


   .. method:: packages(self, category)


      Provide a sequence of package names that provide compatible installations for the given
      package {category}.


   .. method:: info(self, package)


      Return information about the given {package}


   .. method:: contents(self, package)


      Generate a sequence of the contents of the {package}


   .. method:: configure(self, installation)


      Dispatch to the {packageInstance} configuration procedure that is specific to a host
      without a specific package manager



