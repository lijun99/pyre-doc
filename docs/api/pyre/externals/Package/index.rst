:mod:`pyre.externals.Package`
=============================

.. py:module:: pyre.externals.Package


Module Contents
---------------

.. py:class:: Package

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



