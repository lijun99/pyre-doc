:mod:`pyre.ipc.Port`
====================

.. py:module:: pyre.ipc.Port


Module Contents
---------------

.. py:class:: Port

   A mechanism that enables peer processes to draw the attention of the process owning the
   port

   .. method:: open(cls, address, **kwds)
      :classmethod:
      :abstractmethod:


      Attempt to draw the attention of the peer process at {address}


   .. method:: install(cls, **kwds)
      :classmethod:
      :abstractmethod:


      Install and activate a port. Called by the owning process when it is ready to start
      accepting guests



