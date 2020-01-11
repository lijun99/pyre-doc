:mod:`pyre.ipc`
===============

.. py:module:: pyre.ipc


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Channel/index.rst
   Dispatcher/index.rst
   Marshaler/index.rst
   Pickler/index.rst
   Pipe/index.rst
   Port/index.rst
   PortTCP/index.rst
   Scheduler/index.rst
   Selector/index.rst
   Socket/index.rst
   SocketTCP/index.rst


Package Contents
----------------

.. py:class:: foundry(factory, implements=None, tip='', **kwds)

   A decorator for callables that return component classes

   .. attribute:: pyre_tip
      :annotation: = 

      

   .. attribute:: pyre_factory
      

      

   .. attribute:: pyre_implements
      

      

   .. method:: __call__(self, *args, **kwds)



   .. method:: sequify(self, items)
      :classmethod:


      Normalize {items} into a tuple



.. function:: pipe(descriptors=None, **kwds)

   If {descriptors} is not {None}, it is expected to be a pair ({infd}, {outfd}) of already
   open file descriptors; just wrap a channel around them. Otherwise, build a pair of pipes
   suitable for bidirectional communication between two processes on the same host


.. function:: tcp(address)

   Builds a channel over a TCP connection to a server

   The parameter {address} is expected to be convertible to a {pyre.schemata.inet} compatible
   address.


.. function:: port(address=None)

   Establishes a port at {address}


.. function:: inet(spec='')

   Convert {spec} to a {pyre.schemata.inet} address


.. py:class:: dispatcher

   Bases: :class:`pyre.protocol`

   Protocol definition for components that monitor communication channels and invoke handlers
   when activity is detected

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The suggested implementation of the {Dispatcher} protocol


   .. method:: watch(self)


      Enter an indefinite loop of monitoring all registered event sources and invoking the
      registered event handlers


   .. method:: stop(self)


      Stop monitoring all communication channels


   .. method:: alarm(self, interval, call)


      Schedule {call} to be invoked after {interval} elapses. {interval} is expected to be
      a dimensional quantity from {pyre.units} with units of time


   .. method:: whenReadReady(self, channel, call)


      Add {call} to the list of routines to call when {channel} is ready to be read


   .. method:: whenWriteReady(self, channel, call)


      Add {call} to the list of routines to call when {channel} is ready to be written


   .. method:: whenException(self, channel, call)


      Add {call} to the list of routines to call when something exceptional has happened
      to {channel}



.. py:class:: marshaler

   Bases: :class:`pyre.protocol`

   Protocol for components responsible for serializing python objects for transmission to
   other processes

   .. method:: pyre_default(cls, **kwds)
      :classmethod:



   .. method:: recv(self, channel)


      Extract and return one object from {channel}


   .. method:: send(self, item, channel)


      Pack and ship {item} over {channel}



.. function:: pickler()

   A marshaler that uses native python services to serialize objects


.. function:: scheduler()

   A component that enables the construction of applications with event loops


.. function:: selector()

   A scheduler that can listen to file objects


.. function:: newPickler(**kwds)

   A marshaler that uses native python services to serialize objects


.. function:: newScheduler(**kwds)

   A component that enables the construction of applications with event loops


.. function:: newSelector(**kwds)

   A scheduler that can listen to file objects


