:mod:`pyre.timers.PythonTimer`
==============================

.. py:module:: pyre.timers.PythonTimer


Module Contents
---------------

.. py:class:: PythonTimer(**kwds)

   Bases: :class:`pyre.timers.AbstractTimer.AbstractTimer`

   A simple timer implementation based on the facilities from the time module in the python
   standard library

   .. attribute:: _start
      :annotation: = 0

      

   .. attribute:: _accumulatedTime
      :annotation: = 0

      

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



