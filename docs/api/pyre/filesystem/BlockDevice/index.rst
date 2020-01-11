:mod:`pyre.filesystem.BlockDevice`
==================================

.. py:module:: pyre.filesystem.BlockDevice


Module Contents
---------------

.. py:class:: BlockDevice

   Bases: :class:`pyre.filesystem.File.File`

   Representation of block devices, a type of unix device driver

   .. attribute:: marker
      :annotation: = b

      

   .. method:: identify(self, explorer, **kwds)


      Tell {explorer} that it is visiting a block device



