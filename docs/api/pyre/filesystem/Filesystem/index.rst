:mod:`pyre.filesystem.Filesystem`
=================================

.. py:module:: pyre.filesystem.Filesystem


Module Contents
---------------

.. py:class:: Filesystem(metadata=None, **kwds)

   Bases: :class:`pyre.filesystem.Folder.Folder`

   The base class for representing filesystems

   A filesystem is a special {Folder} that maintains an association between the {Nodes} it
   contains and {Info} objects that are dependent on the specific filesystem type and capture
   what the filesystem knows about them.

   .. method:: info(self, node)


      Look up and return the available metadata associated with {node}


   .. method:: checksum(self, node, **kwds)


      Compute a checksum for the node


   .. method:: open(self, node, **kwds)
      :abstractmethod:


      Open the file associated with {node}


   .. method:: discover(self, root=None, **kwds)


      Fill my structure with nodes from an external source


   .. method:: attach(self, node, uri, metadata=None, **kwds)


      Maintenance for the {vnode} table. Filesystems that maintain more elaborate meta-data
      about their nodes must override to build their {info} structures.



