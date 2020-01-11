:mod:`pyre.config.events`
=========================

.. py:module:: pyre.config.events

.. autoapi-nested-parse::

   The various codecs build and populate instances of these classes as part of the ingestion of
   configuration sources. They provide a temporary holding place to store the harvested events
   until the entire source is processed without errors. This way, the configuration retrieved from
   the source will be known to be at least syntactically correct without the risk of polluting the
   global framework configuration data structures with partial input from invalid sources.



Module Contents
---------------

.. py:class:: Event(locator, **kwds)

   The base class for all configuration events

   .. attribute:: locator
      

      


.. py:class:: Command(command, **kwds)

   Bases: :class:`pyre.config.events.Event`

   A command

   .. attribute:: command
      

      

   .. method:: identify(self, inspector, **kwds)


      Ask {inspector} to process a {Command}


   .. method:: __str__(self)




.. py:class:: Assignment(key, value, **kwds)

   Bases: :class:`pyre.config.events.Event`

   A request to bind a {key} to a {value}

   .. attribute:: key
      

      

   .. attribute:: value
      

      

   .. method:: identify(self, inspector, **kwds)


      Ask {inspector} to process an {Assignment}


   .. method:: __str__(self)




.. py:class:: ConditionalAssignment(component, condition, **kwds)

   Bases: :class:`pyre.config.events.Assignment`

   A request to bind a {key} to a {value} subject to a condition

   .. attribute:: component
      

      

   .. attribute:: conditions
      

      

   .. method:: identify(self, inspector, **kwds)


      Ask {inspector} to process a {ConditionalAssignment}


   .. method:: __str__(self)




.. py:class:: Source(source, **kwds)

   Bases: :class:`pyre.config.events.Event`

   A request to load configuration settings from a named source

   .. attribute:: source
      

      

   .. method:: identify(self, inspector, **kwds)


      Ask {inspector} to process a {Source} event


   .. method:: __str__(self)




