:mod:`pyre.timers.AbstractTimer`
================================

.. py:module:: pyre.timers.AbstractTimer


Module Contents
---------------

.. py:class:: AbstractTimer

   Bases: :class:`pyre.patterns.Named.Named`

   Base class for timers

   .. method:: start(self)
      :abstractmethod:


      Start the timer


   .. method:: stop(self)
      :abstractmethod:


      Stop the timer


   .. method:: reset(self)
      :abstractmethod:


      Reset the timer. Resetting a time disables it and clears the accumulated time. The timer
      must be started again before it can read


   .. method:: read(self)
      :abstractmethod:


      Read the time elapsed between a start and a stop, in seconds. The accuracy of the timer is
      determined by the implementation strategy


   .. method:: lap(self)
      :abstractmethod:


      Read the time accumulated by this timer without disturbing it



