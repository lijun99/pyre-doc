:mod:`pyre.platforms.Host`
==========================

.. py:module:: pyre.platforms.Host


Module Contents
---------------

.. py:class:: Host(**kwds)

   Bases: :class:`pyre.component`

   Encapsulation of a generic host

   .. attribute:: hostname
      

      

   .. attribute:: nickname
      

      

   .. attribute:: platform
      

      

   .. attribute:: release
      

      

   .. attribute:: codename
      

      

   .. attribute:: distribution
      

      

   .. attribute:: externals
      

      

   .. attribute:: doc
      :annotation: = a map of package categories to installation instances

      

   .. attribute:: packager
      

      

   .. attribute:: doc
      :annotation: = the manager of external packages installed on this host

      

   .. method:: cpus(self)
      :property:


      The CPU configuration of the machine as a triplet (cpus, physical cores, logical cores)


   .. method:: cpuSurvey(cls)
      :classmethod:


      Collect information about the CPU resources on this host


   .. method:: dynamicLibrary(cls, stem)
      :classmethod:


      Convert the sequence of stems into likely filenames for shared objects


   .. method:: staticLibrary(cls, stem)
      :classmethod:


      Convert the sequence of stems into likely filenames for shared objects


   .. method:: dynamicLibraries(cls, stems)
      :classmethod:


      Convert the sequence of stems into likely filenames for shared objects


   .. method:: staticLibraries(cls, stems)
      :classmethod:


      Convert the sequence of stems into likely filenames for shared objects



