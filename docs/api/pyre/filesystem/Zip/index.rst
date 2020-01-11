:mod:`pyre.filesystem.Zip`
==========================

.. py:module:: pyre.filesystem.Zip


Module Contents
---------------

.. py:class:: Zip(metadata, **kwds)

   Bases: :class:`pyre.filesystem.Filesystem.Filesystem`

   Representation of a filesystem mounted from a zip file on the local host machine

   .. method:: open(self, node, **kwds)


      Open the file associate with {node}


   .. method:: discover(self, root=None, **kwds)


      Populate the filesystem with the contents of the zipfile

      The current implementation does not allow the specification of the number of levels in
      the hierarchy to retrieve, mostly because the interface of the underlying zipfile
      object does not allow for efficient retrievals. This may change in a future
      implementation.



