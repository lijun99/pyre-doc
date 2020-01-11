:mod:`pyre.filesystem.Finder`
=============================

.. py:module:: pyre.filesystem.Finder


Module Contents
---------------

.. py:class:: Finder

   Bases: :class:`pyre.filesystem.Explorer.Explorer`

   A visitor that generates a list of the contents of a filesystem

   .. method:: explore(self, folder, pattern='.*')


      Traverse the folder and return contents that match the given pattern


   .. method:: _explore(self, node, path)


      The recursive workhorse for folder exploration



