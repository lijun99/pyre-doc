:mod:`pyre.platforms.POSIX`
===========================

.. py:module:: pyre.platforms.POSIX


Module Contents
---------------

.. py:class:: POSIX

   Bases: :class:`pyre.platforms.Host.Host`

   Encapsulation of a POSIX host

   .. attribute:: platform
      :annotation: = posix

      

   .. attribute:: distribution
      :annotation: = unknown

      

   .. method:: systemdirs(cls)
      :classmethod:


      Generate a sequence of directories with system wide package installations


   .. method:: which(cls, filename)
      :classmethod:


      Search for {filename} through the list of path prefixes in the {PATH} environment variable



