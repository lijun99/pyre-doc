:mod:`pyre.nexus.Node`
======================

.. py:module:: pyre.nexus.Node


Module Contents
---------------

.. py:class:: Node(**kwds)

   Bases: :class:`pyre.nexus.Peer.Peer`

   .. attribute:: services
      

      

   .. attribute:: doc
      :annotation: = the table of available services

      

   .. attribute:: application
      

      

   .. method:: prepare(self, application)


      Get ready to listen for incoming connections


   .. method:: shutdown(self)


      Shut everything down and exit gracefully


   .. method:: reload(self)


      Reload the nodal configuration for a distributed application


   .. method:: signal(self, signal, frame)


      An adaptor that dispatches {signal} to the registered handler


   .. method:: newSignalIndex(self)


      By default, nodes register handlers for process termination and configuration reload


   .. method:: registerSignalHandlers(self)


      By default, nodes register handlers for process termination and configuration reload



