:mod:`pyre.filesystem.CharacterDevice`
======================================

.. py:module:: pyre.filesystem.CharacterDevice


Module Contents
---------------

.. py:class:: CharacterDevice

   Bases: :class:`pyre.filesystem.File.File`

   Representation of character devices, a type of unix device driver

   .. attribute:: marker
      :annotation: = c

      

   .. method:: identify(self, explorer, **kwds)


      Tell {explorer} that it is visiting a serial device



