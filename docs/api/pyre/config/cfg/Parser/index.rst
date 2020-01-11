:mod:`pyre.config.cfg.Parser`
=============================

.. py:module:: pyre.config.cfg.Parser


Module Contents
---------------

.. py:class:: Parser(**kwds)

   Bases: :class:`pyre.parsing.parser`

   A simple parser for {cfg} files

   This parser understands a variant of the windows {INI} file format. See the package
   documentation for details.

   .. attribute:: name
      :annotation: = []

      

   .. attribute:: family
      :annotation: = []

      

   .. attribute:: productions
      

      

   .. attribute:: configuration
      

      

   .. method:: parse(self, uri, stream, locator)


      Harvest the configuration events in {stream}


   .. method:: processor(self, locator)


      Receive tokens from the scanner and handle them


   .. method:: ignore(self, **kwds)


      Do nothing


   .. method:: context(self, current)


      Process a section fragment and use it to specify the assignment context


   .. method:: assignment(self, current)


      Process a key assignment


   .. method:: handleError(self, description, locator)


      Process the {error}



