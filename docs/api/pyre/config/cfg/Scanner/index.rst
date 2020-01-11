:mod:`pyre.config.cfg.Scanner`
==============================

.. py:module:: pyre.config.cfg.Scanner


Module Contents
---------------

.. py:class:: Scanner

   Bases: :class:`pyre.parsing.scanner`

   Converts an input source into a stream of tokens. The input is expected to conform to a
   simple version of the well-known windows INI format.

   .. attribute:: marker
      

      

   .. attribute:: secbeg
      

      

   .. attribute:: secend
      

      

   .. attribute:: comment
      

      

   .. attribute:: key
      

      

   .. attribute:: value
      

      

   .. method:: pyre_tokenize(self, uri, stream, client)


      Convert the input {stream} into tokens that are not whitespace



