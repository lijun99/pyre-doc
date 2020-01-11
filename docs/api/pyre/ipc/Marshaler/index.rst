:mod:`pyre.ipc.Marshaler`
=========================

.. py:module:: pyre.ipc.Marshaler


Module Contents
---------------

.. py:class:: Marshaler

   Bases: :class:`pyre.protocol`

   Protocol for components responsible for serializing python objects for transmission to
   other processes

   .. method:: pyre_default(cls, **kwds)
      :classmethod:



   .. method:: recv(self, channel)


      Extract and return one object from {channel}


   .. method:: send(self, item, channel)


      Pack and ship {item} over {channel}



