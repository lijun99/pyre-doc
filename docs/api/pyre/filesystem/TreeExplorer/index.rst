:mod:`pyre.filesystem.TreeExplorer`
===================================

.. py:module:: pyre.filesystem.TreeExplorer


Module Contents
---------------

.. py:class:: TreeExplorer(indent=0, **kwds)

   Bases: :class:`pyre.filesystem.Explorer.Explorer`

   A visitor that creates a tree representation with the name and node type of the contents of
   a folder

   .. attribute:: INDENT
      

      

   .. method:: explore(self, node, label)


      Traverse the filesystem and print out its contents


   .. method:: render(self, name, node)




