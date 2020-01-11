:mod:`pyre.parsing.SWScanner`
=============================

.. py:module:: pyre.parsing.SWScanner


Module Contents
---------------

.. py:class:: SWScanner

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



