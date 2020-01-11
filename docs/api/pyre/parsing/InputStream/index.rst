:mod:`pyre.parsing.InputStream`
===============================

.. py:module:: pyre.parsing.InputStream


Module Contents
---------------

.. py:class:: InputStream(uri, stream, line=0, column=0, **kwds)

   A wrapper over input streams that maintains location information

   .. attribute:: uri
      

      

   .. attribute:: stream
      

      

   .. attribute:: line
      :annotation: = 0

      

   .. attribute:: column
      :annotation: = 0

      

   .. attribute:: text
      

      

   .. method:: locator(self)
      :property:


      Build and return a locator to my current position in my input stream


   .. method:: match(self, scanner, tokenizer)


      Attempt to match the text at my current position using the given regular expression


   .. method:: update(self, client=None)


      Prepare to process more text from my input stream



