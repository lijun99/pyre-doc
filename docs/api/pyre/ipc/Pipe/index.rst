:mod:`pyre.ipc.Pipe`
====================

.. py:module:: pyre.ipc.Pipe


Module Contents
---------------

.. py:class:: Pipe(infd, outfd, **kwds)

   Bases: :class:`pyre.ipc.Channel.Channel`

   A channel that uses pipes as the communication mechanism

   .. attribute:: infd
      

      

   .. attribute:: outfd
      

      

   .. method:: open(cls, **kwds)
      :classmethod:


      Build a pair of pipes that are suitable for bidirectional communication between two
      processes


   .. method:: close(self)


      Shut down this channel


   .. method:: inbound(self)
      :property:


      Retrieve the channel end point that can be read


   .. method:: outbound(self)
      :property:


      Retrieve the channel end point that can be written


   .. method:: read(self, minlen=0, maxlen=64 * 1024)


      Read {count} bytes from my input channel


   .. method:: write(self, bstr)


      Write the bytes in {bstr} to my output channel


   .. method:: __str__(self)




