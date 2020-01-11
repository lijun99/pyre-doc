:mod:`pyre.http.Request`
========================

.. py:module:: pyre.http.Request


Module Contents
---------------

.. py:class:: Request

   Parse and analyze an HTTP request

   .. attribute:: url
      

      

   .. attribute:: command
      

      

   .. attribute:: version
      

      

   .. attribute:: headers
      

      

   .. attribute:: payload
      

      

   .. attribute:: described
      :annotation: = False

      

   .. attribute:: complete
      :annotation: = False

      

   .. attribute:: HEADER_ENCODING
      :annotation: = iso-8859-1

      

   .. attribute:: blank
      

      

   .. attribute:: keyval
      

      

   .. attribute:: protocol
      

      

   .. method:: extract(self, server, chunk)


      Process a {chunk} of bytes


   .. method:: extractHeaders(self, server, chunk)


      Extract RFC2822 headers from the bytes sent by the peer


   .. method:: extractPayload(self, server, chunk, offset)


      Extract a {chunk} of bytes and store them


   .. method:: dump(self, channel, indent='', showHeaders=True, showPayload=True)


      Place debugging information in the given channel



