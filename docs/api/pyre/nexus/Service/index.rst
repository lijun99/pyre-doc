:mod:`pyre.nexus.Service`
=========================

.. py:module:: pyre.nexus.Service


Module Contents
---------------

.. py:class:: Service

   Bases: :class:`pyre.protocol`

   Protocol definition for components that handle events in communication channels

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The suggested implementation of the {Service} protocol


   .. method:: activate(self, application, dispatcher)


      Prepare to start receiving information from the network


   .. method:: acknowledge(self, dispatcher, channel)


      A peer has attempted to establish a connection


   .. method:: validate(self, channel, address)


      Examine the peer {address} and determine whether to continue the conversation


   .. method:: connect(self, dispatcher, channel, address)


      Prepare to start accepting requests from a new peer


   .. method:: process(self, dispatcher, channel)


      Start or continue a conversation with a peer over {channel}


   .. method:: shutdown(self)


      Clean up and shutdown



