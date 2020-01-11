:mod:`pyre.ipc.SocketTCP`
=========================

.. py:module:: pyre.ipc.SocketTCP


Module Contents
---------------

.. py:class:: SocketTCP

   Bases: :class:`pyre.ipc.Socket.Socket`

   A channel that uses TCP sockets as the communication mechanism

   .. attribute:: type
      

      

   .. attribute:: __slots__
      :annotation: = []

      

   .. method:: read(self, minlen=0, maxlen=4 * 1024)


      Read {count} bytes from my input channel


   .. method:: write(self, bstr)


      Write the bytes in {bstr} to my output channel


   .. method:: __str__(self)




