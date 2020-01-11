:mod:`pyre.config.pfg.Parser`
=============================

.. py:module:: pyre.config.pfg.Parser


Module Contents
---------------

.. py:class:: Parser(**kwds)

   Bases: :class:`pyre.parsing.parser`

   A simple parser for {pfg} files

   This parser understands a file format that uses whitespace to capture the hierarchical
   structure of the input

   .. attribute:: errors
      

      

   .. attribute:: productions
      

      

   .. attribute:: configuration
      

      

   .. method:: parse(self, uri, stream, locator)


      Harvest the configuration events in {stream}


   .. method:: processor(self, locator)


      Receive tokens from the scanner and handle them


   .. method:: ignore(self, **kwds)


      Do nothing


   .. method:: section(self, token)


      Process a section fragment and use it to specify the assignment context


   .. method:: assignment(self, token)


      Process a key assignment


   .. method:: value(self, token)


      Process the value portion of an assignment


   .. method:: pop(self, token)


      Process the closing of a block


   .. method:: handleError(self, description, locator)


      Process the {error}



