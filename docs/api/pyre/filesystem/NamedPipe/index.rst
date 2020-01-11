:mod:`pyre.filesystem.NamedPipe`
================================

.. py:module:: pyre.filesystem.NamedPipe


Module Contents
---------------

.. py:class:: NamedPipe

   Bases: :class:`pyre.filesystem.File.File`

   Representation of named pipes, a unix interprocess communication mechanism

   .. attribute:: marker
      :annotation: = p

      

   .. method:: identify(self, explorer, **kwds)


      Tell {explorer} that it is visiting a FIFO



