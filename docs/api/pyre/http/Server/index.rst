:mod:`pyre.http.Server`
=======================

.. py:module:: pyre.http.Server


Module Contents
---------------

.. py:class:: Server(**kwds)

   Bases: :class:`pyre.nexus.server`

   A server that understands HTTP

   .. attribute:: renderer
      

      

   .. attribute:: doc
      :annotation: = the renderer of the server responses to client requests

      

   .. attribute:: requests
      

      

   .. attribute:: MAX_BYTES
      

      

   .. method:: name(self)
      :property:


      Server identification


   .. method:: version(self)
      :property:


      Server version


   .. method:: process(self, channel)


      Initiate or continue a conversation with a peer over {channel}


   .. method:: fulfill(self, request)


      Fulfill the given fully formed client {request}


   .. method:: respond(self, channel, response)




