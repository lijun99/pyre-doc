:mod:`pyre.platforms.Linux`
===========================

.. py:module:: pyre.platforms.Linux


Module Contents
---------------

.. py:class:: Linux

   Bases: :class:`pyre.platforms.POSIX.POSIX`

   Encapsulation of a generic linux host

   .. attribute:: platform
      :annotation: = linux

      

   .. attribute:: distribution
      :annotation: = generic

      

   .. attribute:: prefix_library
      :annotation: = lib

      

   .. attribute:: extension_staticLibrary
      :annotation: = .a

      

   .. attribute:: extension_dynamicLibrary
      :annotation: = .so

      

   .. attribute:: template_staticLibrary
      :annotation: = {0.prefix_library}{1}{0.extension_staticLibrary}

      

   .. attribute:: template_dynamicLibrary
      :annotation: = {0.prefix_library}{1}{0.extension_dynamicLibrary}

      

   .. attribute:: issue
      :annotation: = /etc/issue

      

   .. attribute:: cpuinfo
      :annotation: = /proc/cpuinfo

      

   .. method:: flavor(cls)
      :classmethod:


      Return a suitable default encapsulation of the runtime host


   .. method:: cpuSurvey(cls)
      :classmethod:


      Collect information about the CPU resources on this host


   .. method:: lscpu(cls)
      :classmethod:


      Invoke {lscpu} to gather CPU info


   .. method:: procCPUInfo(cls)
      :classmethod:


      Interrogate /proc for CPU info

      This was the original manner in which pyre discovered cpu information. It appears that
      the gathering of information was inadvertently polluted by what is available for
      {x86_64} architectures, and fails to be useful on {ppc64le}. As a result, it has been
      replaced by the method {lscpu} above that seems to slower but much more reliable.


   .. method:: tokenizeCPUInfo(cls, cpuinfo)
      :classmethod:


      Split the CPU info file into (key, value) pairs



