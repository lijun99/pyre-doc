:mod:`pyre.ipc.Channel`
=======================

.. py:module:: pyre.ipc.Channel


Module Contents
---------------

.. py:class:: Channel

   A wrapper around the lower level IPC mechanisms that normalizes the sending and receiving
   of messages. See {Pipe} and {Socket} for concrete examples of encapsulation of the
   operating system services.

   .. method:: open(cls, **kwds)
      :classmethod:
      :abstractmethod:


      Channel factory


   .. method:: close(self)
      :abstractmethod:


      Shutdown the channel


   .. method:: inbound(self)
      :property:


      Retrieve the channel end point that can be read


   .. method:: outbound(self)
      :property:


      Retrieve the channel end point that can be written


   .. method:: read(self, minlen, maxlen)
      :abstractmethod:


      Read up to {count} bytes from my input channel


   .. method:: write(self, bstr)
      :abstractmethod:


      Write the bytes in {bstr} to output channel



