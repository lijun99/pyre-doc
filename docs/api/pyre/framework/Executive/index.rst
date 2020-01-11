:mod:`pyre.framework.Executive`
===============================

.. py:module:: pyre.framework.Executive


Module Contents
---------------

.. py:class:: Executive(**kwds)

   The specification of the obligations of the various managers of framework services

   .. attribute:: hostmapkey
      :annotation: = pyre.hostmap

      

   .. attribute:: nameserver
      

      

   .. attribute:: fileserver
      

      

   .. attribute:: registrar
      

      

   .. attribute:: configurator
      

      

   .. attribute:: linker
      

      

   .. attribute:: timekeeper
      

      

   .. attribute:: host
      

      

   .. attribute:: user
      

      

   .. attribute:: terminal
      

      

   .. attribute:: environ
      

      

   .. attribute:: errors
      

      

   .. method:: loadConfiguration(self, uri, locator=None, priority=priority.user)


      Load configuration settings from {uri} and insert them in the configuration database
      with the given {priority}.


   .. method:: newTimer(self, **kwds)


      Build an return a timer


   .. method:: configure(self, stem, locator, priority)


      Locate and load all accessible configuration files for the given {stem}


   .. method:: resolve(self, uri, protocol=None, **kwds)


      Interpret {uri} as a component descriptor and attempt to resolve it

      {uri} encodes the descriptor using the URI specification
          scheme://authority/address#name
      where
          {scheme}: the resolution mechanism
          {authority}: the process that will perform the resolution
          {address}: the location of the component descriptor
          {name}: the optional name to use when instantiating the retrieved descriptor

      Currently, there is support for two classes of schemes:

      The "import" scheme requires that the component descriptor is accessible on the python
      path. The corresponding codec interprets {address} as two parts: {package}.{symbol},
      with {symbol} being the trailing part of {address} after the last '.'. The codec then
      uses the interpreter to import the {symbol} using {address} to access the containing
      module. For example, the {uri}

          import:gauss.shapes.box

      is treated as if the following statement had been issued to the interpreter

          from gauss.shapes import box

      Any other scheme specification is interpreted as a request for a file based component
      factory. The {address} is again split into two parts: {path}/{symbol}, where {symbol}
      is the trailing part after the last '/' separator. The codec assumes that {path} is a
      valid path in the physical or logical filesystems managed by the
      {executive.fileserver}, and that it contains executable python code that provides the
      definition of the required symbol.  For example, the {uri}

          vfs:/local/shapes.py/box

      implies that the fileserver can resolve the address {local/shapes.py} into a valid file
      within the virtual filesystem that forms the application namespace. The referenced
      {symbol} must be a callable that can produce component class records when called. For
      example, the file {shapes.py} might contain

          import pyre
          class box(pyre.component): pass

      which exposes a component class {box} that has the right name and whose constructor can
      be invoked to produce component instances. If you prefer to place such declarations
      inside functions, e.g. to avoid certain name collisions, you can use mark your function
      as a component {foundry} by decorating as follows:

          @pyre.foundry(implements=())
          def box():
              class box(pyre.component): pass
              return box


   .. method:: retrieveComponents(self, uri)


      Retrieve all component classes from the shelf at {uri}


   .. method:: retrieveComponentDescriptor(self, uri, protocol, **kwds)


      The component resolution workhorse


   .. method:: registerProtocolClass(self, protocol, family, locator)


      Register a freshly minted protocol class


   .. method:: registerComponentClass(self, component, family)


      Register a freshly minted component class


   .. method:: registerComponentInstance(self, instance, name)


      Register a freshly minted component instance


   .. method:: registerPackage(self, name, file)


      Register a {pyre} package


   .. method:: newNameServer(self, **kwds)


      Build a new name server


   .. method:: newFileServer(self, **kwds)


      Build a new file server


   .. method:: newComponentRegistrar(self, **kwds)


      Build a new component registrar


   .. method:: newConfigurator(self, **kwds)


      Build a new configuration event processor


   .. method:: newLinker(self, **kwds)


      Build a new configuration event processor


   .. method:: newCommandLineParser(self, **kwds)


      Build a new parser of command line arguments


   .. method:: newSchema(self, **kwds)


      Build a new schema manager


   .. method:: newTimerRegistry(self, **kwds)


      Build a new time registrar


   .. method:: boot(self)


      Perform the final framework initialization step


   .. method:: activate(self)


      Turn on the executive


   .. method:: discover(self, **kwds)


      Discover what is known about the runtime environment


   .. method:: initializeNamespaces(self)


      Create and initialize the default namespace entries


   .. method:: shutdown(self)


      Clean up


   .. method:: _configurationLoader(self, key, value, locator)


      Handler for the {config} command line argument



