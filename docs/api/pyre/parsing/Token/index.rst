:mod:`pyre.parsing.Token`
=========================

.. py:module:: pyre.parsing.Token


Module Contents
---------------

.. py:class:: Token(lexeme='', locator=None, **kwds)

   Base class for tokens, the atomic units of recognizable text in a stream

   .. attribute:: name
      :annotation: = 

      

   .. attribute:: head
      :annotation: = 

      

   .. attribute:: tail
      :annotation: = 

      

   .. attribute:: pattern
      

      

   .. attribute:: regex
      :annotation: = 

      

   .. attribute:: scanner
      

      

   .. attribute:: __slots__
      :annotation: = ['lexeme', 'locator']

      

   .. method:: __len__(self)


      Compute the length of the lexeme

      N.B.: this is not the same as the footprint of the token in the input stream, which
      includes the {head} and {tail} of the token


   .. method:: __str__(self)


      Textual representation, mostly for debugging purposes



