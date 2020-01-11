:mod:`pyre.ipc.Scheduler`
=========================

.. py:module:: pyre.ipc.Scheduler


Module Contents
---------------

.. py:class:: Scheduler(**kwds)

   Bases: :class:`pyre.component`

   Support for invoking event handlers at specified times

   Clients create alarms by invoking {alarm} and supplying an event handler to be invoked and
   specifying the number of seconds before the alarm comes due. The time interval is expected
   to be a dimensional quantity with units of time.

   The current implementation converts the time interval before the alarm comes due into an
   absolute time, and pairs it with the handler into an {_alarm} instance. The {_alarm} is
   then stored into a list of such {_alarms}, and the list is sorted in reverse order,
   i.e. with the alarm that is due next at the end of the list.

   .. py:class:: _alarm(time, handler)

      Encapsulate the time and event handler of an alarm

      .. attribute:: __slots__
         :annotation: = ['time', 'handler']

         

      .. method:: __str__(self)




   .. attribute:: _alarms
      

      

   .. method:: alarm(self, interval, call)


      Schedule {call} to be invoked after {interval} elapses.

      parameters:
         {call}: a function that takes the current time and returns a reschedule interval
         {interval}: a dimensional quantity from {pyre.units} with units of time


   .. method:: poll(self)


      Compute the number of seconds until the next alarm comes due.

      If there are no scheduled alarms, {poll} returns {None}; if alarms are overdue, it
      returns 0. This slightly strange logic is designed to satisfy the requirements for
      calling {select}.


   .. method:: awaken(self)


      Raise all overdue alarms by calling the registered handlers



