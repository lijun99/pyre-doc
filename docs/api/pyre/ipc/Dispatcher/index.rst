:mod:`pyre.ipc.Dispatcher`
==========================

.. py:module:: pyre.ipc.Dispatcher


Module Contents
---------------

.. py:class:: Dispatcher

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



