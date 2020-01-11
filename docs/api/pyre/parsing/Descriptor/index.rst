:mod:`pyre.parsing.Descriptor`
==============================

.. py:module:: pyre.parsing.Descriptor


Module Contents
---------------

.. py:class:: Descriptor(pattern=None, head='', tail='', **kwds)

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



