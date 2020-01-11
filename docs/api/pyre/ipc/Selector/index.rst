:mod:`pyre.ipc.Selector`
========================

.. py:module:: pyre.ipc.Selector


Module Contents
---------------

.. py:class:: Selector(**kwds)

   Bases: :class:`pyre.ipc.Scheduler.Scheduler`

   An event demultiplexer implemented using the {select} system call.

   In addition to supporting alarms via its {Scheduler} base class, {Selector} monitors
   changes in the state of channels. Processes that hold {Selector} instances can go to sleep
   until either an alarm rings or a channel is ready for IO, at which point {Selector} invokes
   whatever handler is associated with the event.

   .. py:class:: _event(channel, handler)

      Encapsulate a channel and the associated call-back

      .. attribute:: __slots__
         :annotation: = ['channel', 'handler']

         


   .. attribute:: _watching
      :annotation: = True

      

   .. method:: whenReadReady(self, channel, call)


      Add {call} to the list of routines to call when {channel} is ready to be read


   .. method:: whenWriteReady(self, channel, call)


      Add {call} to the list of routines to call when {channel} is ready to be written


   .. method:: whenException(self, channel, call)


      Add {call} to the list of routines to call when something exceptional has happened
      to {channel}


   .. method:: stop(self)


      Request the selector to stop watching for further events


   .. method:: watch(self)


      Enter an indefinite loop of monitoring all registered event sources and invoking the
      registered event handlers


   .. method:: dispatch(self, index, entities)


      Invoke the handlers registered in {index} that are associated with the descriptors in
      {entities}



