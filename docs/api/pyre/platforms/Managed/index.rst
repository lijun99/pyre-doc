:mod:`pyre.platforms.Managed`
=============================

.. py:module:: pyre.platforms.Managed


Module Contents
---------------

.. py:class:: Managed

   Bases: :class:`pyre.component`

   Support for un*x systems that don't have package management facilities

   .. attribute:: _prefix
      

      

   .. method:: name(self)
      :property:


      Get the name of this package manager


   .. method:: client(self)
      :property:


      Get the name of the front end to the package manager database


   .. method:: prefix(self)


      Retrieve the package manager install location


   .. method:: installed(self)


      Retrieve available information for all installed packages


   .. method:: info(self, package)


      Return the available information about {package}


   .. method:: packages(self, category)


      Provide a sequence of package names that provide compatible installations for the given
      package {category}.


   .. method:: contents(self, package)


      Retrieve the contents of the {package}


   .. method:: configure(self, installation)


      Dispatch to the {installation} configuration procedure that is specific to this package
      manager


   .. method:: find(self, target, pile)


      Interpret {target} as a regular expression and return a sequence of the contents of {pile}
      that match it.

      This is intended as a way to scan through the contents of packages to find a path that
      matches {target}


   .. method:: findfirst(self, target, contents)


      Locate the path to {target} in the {contents} of some package


   .. method:: locate(self, targets, paths)


      Generate a sequence of the full {paths} to the {targets}



