:mod:`pyre.parsing.Scanner`
===========================

.. py:module:: pyre.parsing.Scanner


Module Contents
---------------

.. py:class:: Scanner

   The input stream tokenizer

   .. attribute:: start
      

      

   .. attribute:: finish
      

      

   .. attribute:: whitespace
      

      

   .. attribute:: pyre_tokens
      

      

   .. attribute:: pyre_tokenizer
      

      

   .. attribute:: pyre_stream
      

      

   .. attribute:: pyre_client
      

      

   .. attribute:: pyre_cache
      

      

   .. method:: pyre_tokenize(self, uri, stream, client)


      Extract lines from {stream}, convert them into token streams and send them to {client}


   .. method:: pyre_start(self)


      Indicate the beginning of scanning


   .. method:: pyre_finish(self)


      Indicate that scanning is complete


   .. method:: pyre_pushback(self, token)


      Push a token back into the token stream


   .. method:: pyre_newline(self, stream)


      Hook invoked when a new line of text is pulled from the input stream


   .. method:: pyre_ignoreWhitespace(self, client)


      Remove {whitespace} tokens from the input stream



