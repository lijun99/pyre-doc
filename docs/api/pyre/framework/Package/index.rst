:mod:`pyre.framework.Package`
=============================

.. py:module:: pyre.framework.Package


Module Contents
---------------

.. py:class:: Package(locator, **kwds)

   Bases: :class:`pyre.patterns.Named.Named`

   The resting place of information collected while loading packages

   .. attribute:: home
      

      

   .. attribute:: prefix
      

      

   .. attribute:: defaults
      

      

   .. attribute:: locator
      

      

   .. attribute:: sources
      

      

   .. attribute:: protocols
      

      

   .. attribute:: components
      

      

   .. attribute:: DEFAULTS
      :annotation: = defaults

      

   .. method:: register(self, executive, file)


      Deduce the package geography based on the location of the importable and add the package
      configuration folder to the pyre configuration path


   .. method:: layout(self)


      Easy access to the package folders


   .. method:: configure(self, executive)


      Locate and ask the executive to load my configuration files


   .. method:: __str__(self)




