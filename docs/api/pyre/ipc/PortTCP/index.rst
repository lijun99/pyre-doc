:mod:`pyre.ipc.PortTCP`
=======================

.. py:module:: pyre.ipc.PortTCP


Module Contents
---------------

.. py:class:: PortTCP(channel, address, **kwds)

   Bases: :class:`pyre.ipc.Port.Port`, :class:`pyre.ipc.Channel.Channel`

   An implementation of a process bell using a TCP port

   .. attribute:: type
      

      

   .. attribute:: channel
      

      

   .. attribute:: address
      

      

   .. method:: open(cls, address, **kwds)
      :classmethod:


      Establish a connection to the remote process at {address}


   .. method:: install(cls, address=None)
      :classmethod:


      Attempt to acquire a port and start listening for connections


   .. method:: inbound(self)
      :property:


      Retrieve the input endpoint of the channel.

      {PortTCP} only implements the portion of the {Channel} interface that is required for
      detecting incoming connections.


   .. method:: close(self)


      Close the port


   .. method:: accept(self)


      Wait until a peer process attempts to open the port and build a communication channel
      with it


   .. method:: __str__(self)




