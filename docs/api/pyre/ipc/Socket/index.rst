:mod:`pyre.ipc.Socket`
======================

.. py:module:: pyre.ipc.Socket


Module Contents
---------------

.. py:class:: Socket

   Bases: :class:`socket.socket`, :class:`pyre.ipc.Channel.Channel`

   A channel that uses sockets as the communication mechanism

   This class captures the part of the {socket} interface that is independent of the type of
   socket. The implementation of the remainder of the {Channel} interface is provided by
   subclasses.

   .. attribute:: __slots__
      :annotation: = []

      

   .. method:: inbound(self)
      :property:


      Retrieve the channel end point that can be read


   .. method:: outbound(self)
      :property:


      Retrieve the channel end point that can be written


   .. method:: peer(self)
      :property:


      Return the address of my peer, i.e. the remote endpoint of the socket


   .. method:: accept(self)


      Wait for a connection attempt, build a channel around the socket to the peer, and
      return it along with the address of the remote process


   .. method:: __str__(self)




