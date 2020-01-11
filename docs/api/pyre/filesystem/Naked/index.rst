:mod:`pyre.filesystem.Naked`
============================

.. py:module:: pyre.filesystem.Naked


Module Contents
---------------

.. py:class:: Naked(uri, **kwds)

   A thin wrapper around local regular files

   .. attribute:: isFolder
      :annotation: = False

      

   .. method:: marker(self)
      :property:


      Return my distinguishing mark used by explorers to decorate their reports


   .. method:: open(self, **kwds)


      Open the file


   .. method:: metadata(self, uri, **kwds)


      Build a structure to hold the node metadata



