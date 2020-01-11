:mod:`pyre.filesystem.SimpleExplorer`
=====================================

.. py:module:: pyre.filesystem.SimpleExplorer


Module Contents
---------------

.. py:class:: SimpleExplorer(indent=0, **kwds)

   Bases: :class:`pyre.filesystem.Explorer.Explorer`

   A visitor that creates an indented list of the name and node type of the contents of a
   filesystem

   .. attribute:: INDENT
      

      

   .. method:: explore(self, node, label)


      Traverse the filesystem and print out its contents


   .. method:: render(self, name, node)




