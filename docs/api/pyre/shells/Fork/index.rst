:mod:`pyre.shells.Fork`
=======================

.. py:module:: pyre.shells.Fork


Module Contents
---------------

.. py:class:: Fork

   Bases: :class:`pyre.shells.Executive.Executive`

   A shell that invokes the main application behavior in a child process

   .. attribute:: capture
      

      

   .. attribute:: doc
      :annotation: = control whether to create communication channels to the daemon process

      

   .. method:: launch(self, application, *args, **kwds)


      Invoke the {application} behavior in a subprocess and return a pair of channels
      corresponding to {stdout} and {stderr} of the child, with the write end of the channels
      both connected to the child's {stdin}


   .. method:: openCommunicationPipes(self)


      Build three pipes for parent/child communication


   .. method:: parentChannels(self, pipes)


      Build the parent side of the communication channels


   .. method:: childChannels(self, pipes)


      Build the child side of the communication channels



