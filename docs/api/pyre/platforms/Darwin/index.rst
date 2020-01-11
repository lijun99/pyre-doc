:mod:`pyre.platforms.Darwin`
============================

.. py:module:: pyre.platforms.Darwin


Module Contents
---------------

.. py:class:: Darwin(**kwds)

   Bases: :class:`pyre.platforms.POSIX.POSIX`

   Encapsulation of a darwin host

   .. attribute:: platform
      :annotation: = darwin

      

   .. attribute:: distribution
      :annotation: = osx

      

   .. attribute:: prefix_library
      :annotation: = lib

      

   .. attribute:: extension_staticLibrary
      :annotation: = .a

      

   .. attribute:: extension_dynamicLibrary
      :annotation: = .dylib

      

   .. attribute:: template_staticLibrary
      :annotation: = {0.prefix_library}{1}{0.extension_staticLibrary}

      

   .. attribute:: template_dynamicLibrary
      :annotation: = {0.prefix_library}{1}{0.extension_dynamicLibrary}

      

   .. attribute:: packager
      

      

   .. attribute:: doc
      :annotation: = the manager of external packages installed on this host

      

   .. attribute:: codenames
      

      

   .. method:: cpuSurvey(cls)
      :classmethod:


      Collect information about the CPU resources on this host


   .. method:: getOSInfo(cls)
      :classmethod:




