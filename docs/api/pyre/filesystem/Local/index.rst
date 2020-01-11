:mod:`pyre.filesystem.Local`
============================

.. py:module:: pyre.filesystem.Local


Module Contents
---------------

.. py:class:: Local(walker, recognizer, **kwds)

   Bases: :class:`pyre.filesystem.Filesystem.Filesystem`

   An encapsulation of a filesystem mounted directly on the local host machine

   .. attribute:: walker
      

      

   .. attribute:: recognizer
      

      

   .. method:: checksum(self, node, **kwds)


      Compute a checksum for the node


   .. method:: open(self, node, **kwds)


      Open the file associated with {node}


   .. method:: mkdir(self, name, parent=None, **kwds)


      Create a subdirectory {name} in {parent}


   .. method:: touch(self, name, parent=None, **kwds)


      Create a file {name} in directory {parent}


   .. method:: write(self, name, contents, parent=None, mode='w')


      Create the file {name} in the folder {parent} with the given {contents}


   .. method:: make(self, name, tree, root=None, **kwds)


      Duplicate the hierarchical structure in {tree} within my context


   .. method:: unlink(self, node, **kwds)


      Remove {node} and its associated file from this filesystem


   .. method:: discover(self, root=None, walker=None, recognizer=None, levels=None, **kwds)


      Traverse the local filesystem starting with {root} and refresh my contents so that they
      match the underlying filesystem



