:mod:`pyre.nexus.Server`
========================

.. py:module:: pyre.nexus.Server


Module Contents
---------------

.. py:class:: Server

   Bases: :class:`pyre.component`

   The base class for network servers

   .. attribute:: address
      

      

   .. attribute:: application
      

      

   .. attribute:: dispatcher
      

      

   .. method:: activate(self, application, dispatcher)


      Grab a port and register it with the event dispatcher


   .. method:: acknowledge(self, channel)


      A peer has attempted to establish a connection


   .. method:: validate(self, channel, address)


      Examine the peer {address} and determine whether to continue the conversation


   .. method:: connect(self, channel, address)


      Prepare to start accepting requests from peers


   .. method:: process(self, channel)


      Say something to the peer


   .. method:: shutdown(self)


      Clean up and shutdown



