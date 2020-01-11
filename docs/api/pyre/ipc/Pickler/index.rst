:mod:`pyre.ipc.Pickler`
=======================

.. py:module:: pyre.ipc.Pickler


Module Contents
---------------

.. py:class:: Pickler

   Bases: :class:`pyre.component`

   A marshaler that uses the native python services in {pickle} to serialize python objects
   for transmission to other processes.

   The {send} protocol pickles an object into the payload byte stream, and builds a header
   with the length of the payload. Similarly, {recv} first extracts the length of the byte
   string and uses that information to pull the object representation from the input
   channel. This is necessary to simplify interacting with streams that may make only portions
   of their contents available at a time.

   .. attribute:: packing
      :annotation: = <L

      

   .. attribute:: headerSize
      

      

   .. method:: send(self, item, channel)


      Pack and ship {item} over {channel}


   .. method:: recv(self, channel)


      Extract and return a single item from {channel}



