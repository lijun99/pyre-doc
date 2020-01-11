:mod:`pyre.timers.NativeTimer`
==============================

.. py:module:: pyre.timers.NativeTimer


Module Contents
---------------

.. py:class:: NativeTimer(name, **kwds)

   Bases: :class:`pyre.timers.AbstractTimer.AbstractTimer`

   Timer implementation that relies on the timer extension module

   .. attribute:: _timer
      

      

   .. method:: start(self)


      Start the timer


   .. method:: stop(self)


      Stop the timer


   .. method:: reset(self)


      Reset the timer.

      This sets the time accumulated by this timer to zero and disables it


   .. method:: read(self)


      Return the total time this timer has been running


   .. method:: lap(self)


      Read the total time this timer has been running without disturbing it



