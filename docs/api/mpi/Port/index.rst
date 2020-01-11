:mod:`mpi.Port`
===============

.. py:module:: mpi.Port


Module Contents
---------------

.. py:class:: Port(peer, tag=tag, communicator=communicator, **kwds)

   Bases: :class:`mpi.Object.Object`

   A simple point-to-point communication conduit for a pair of processes

   .. attribute:: peer
      

      

   .. attribute:: tag
      :annotation: = 0

      

   .. attribute:: communicator
      

      

   .. method:: recv(self)


      Receive a python object from my peer


   .. method:: send(self, item)


      Pack and send {item} to my peer


   .. method:: recvString(self)


      Receive a string from my peer


   .. method:: sendString(self, string)


      Send a string to my peer



