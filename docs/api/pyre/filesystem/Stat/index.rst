:mod:`pyre.filesystem.Stat`
===========================

.. py:module:: pyre.filesystem.Stat


Module Contents
---------------

.. py:class:: Stat

   Bases: :class:`pyre.filesystem.Recognizer.Recognizer`

   This class provides support for sorting out local filesystem entries based on the lowest
   level of metadata available: the actual representation on the hard disk.

   .. attribute:: filetypes
      

      

   .. method:: recognize(cls, entry, follow_symlinks=False)
      :classmethod:


      The most basic file recognition: convert the name of a file into a {Node} descendant
      and decorate it with all the meta-data available on the disk.



