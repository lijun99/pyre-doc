:mod:`pyre.filesystem.Node`
===========================

.. py:module:: pyre.filesystem.Node


Module Contents
---------------

.. py:class:: Node(filesystem, **kwds)

   The base class for all filesystem entries

   {Node} and {Folder} are the leaf and container types for the composite that enables the
   representation of the hierarchical structure of filesystems.

   .. attribute:: isFolder
      :annotation: = False

      

   .. method:: info(self)
      :property:


      Return whatever metadata the filesystem maintains about me


   .. method:: uri(self)
      :property:


      Return my location relative to the root of my filesystem


   .. method:: marker(self)
      :property:


      Return my distinguishing mark used by explorers to decorate their reports


   .. method:: checksum(self, **kwds)


      Build a checksum that summarizes my contents


   .. method:: open(self, **kwds)


      Access the contents of the physical resource with which I am associated


   .. method:: dump(self, indent=0)


      Print out my contents using a tree explorer


   .. method:: print(self)


      Display my contents



