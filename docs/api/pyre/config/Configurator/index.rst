:mod:`pyre.config.Configurator`
===============================

.. py:module:: pyre.config.Configurator


Module Contents
---------------

.. py:class:: Configurator(executive=None, **kwds)

   The manager of the configuration store

   .. attribute:: locator
      

      

   .. attribute:: codecs
      

      

   .. method:: loadConfiguration(self, uri, source, locator, priority)


      Use {uri} to find a codec that can process {source} into a stream of configuration
      events


   .. method:: codec(self, encoding)


      Retrieve the codec associated with the given {encoding}


   .. method:: register(self, codec)


      Add {codec} to my registry


   .. method:: encodings(self)


      Return the registered encodings


   .. method:: processEvents(self, events, priority)


      Iterate over the {configuration} events and insert them into the model at the given
      {priority} level


   .. method:: assign(self, assignment, priority)


      Process {assignment} by building a slot and placing it in the nameserver


   .. method:: defer(self, assignment, priority)


      Process a conditional assignment


   .. method:: execute(self, command, priority)


      Record a request to execute a command


   .. method:: load(self, request, priority)


      Ask the pyre executive to load the configuration settings in {source}


   .. method:: configureComponentClass(self, component)


      The last step in the configuration of a component class


   .. method:: configureComponentInstance(self, instance)


      The last step in the configuration of a component instance


   .. method:: retrieveDirectAssignments(self, key)


      Locate the direct configuration assignment under {key}


   .. method:: retrieveDeferredAssignments(self, key)


      Locate the deferred assignments that are relevant to the component instance associated
      with the supplied configuration {key}


   .. method:: initializeNamespace(self)


      Place my default settings in the global namespace


   .. method:: _indexDefaultCodecs(self)


      Initialize the codec index



