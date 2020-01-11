:mod:`pyre.parsing`
===================

.. py:module:: pyre.parsing

.. autoapi-nested-parse::

   This package provides support for writing simple parsers



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Descriptor/index.rst
   InputStream/index.rst
   Lexer/index.rst
   Parser/index.rst
   SWScanner/index.rst
   Scanner/index.rst
   Token/index.rst
   exceptions/index.rst


Package Contents
----------------

.. py:class:: token(pattern=None, head='', tail='', **kwds)

   Place holders for the token specifications

   Descriptors are harvested by {Lexer}, the metaclass of {Scanner} subclasses, and converted
   into subclasses of {Token}

   .. attribute:: head
      :annotation: = 

      

   .. attribute:: tail
      :annotation: = 

      

   .. attribute:: pattern
      :annotation: = 

      

   .. method:: __str__(self)


      Build a representation of the descriptor, mostly for debugging purposes



.. py:class:: scanner

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



.. py:class:: sws

   Bases: :class:`pyre.parsing.Scanner.Scanner`

   A scanner for languages that use leading whitespace to indicate the hierarchical structure
   of the content

   .. attribute:: pop
      

      

   .. attribute:: push
      

      

   .. attribute:: cdata
      

      

   .. attribute:: comment
      

      

   .. attribute:: pyre_dent
      :annotation: = 0

      

   .. attribute:: pyre_blocks
      

      

   .. attribute:: margin
      

      

   .. method:: pyre_start(self)


      Scanning has begun


   .. method:: pyre_finish(self)


      Scanning has ended


   .. method:: pyre_newline(self, stream)


      A fresh line has been retrieved from the input {stream}


   .. method:: pyre_indent(self, locator, column)


      Indent to the given {column}


   .. method:: pyre_dedent(self, locator, column)


      Dedent by as many open blocks as it takes to come back to {column}


   .. method:: pyre_cdata(self)


      Scan forward from the current location and convert any text in all nested blocks into a
      {cdata} token. The lexeme of a {cdata} token is a list of strings with the leading
      indentation, all trivial lines, and all embedded comments removed.


   .. method:: pyre_trim(self, text)


      Determine whether {text} contains any structurally relevant information



.. py:class:: parser(**kwds)

   The base class for parsers

   .. attribute:: lexer
      

      

   .. attribute:: scanner
      

      


