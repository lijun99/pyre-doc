:mod:`pyre.components.Tracker`
==============================

.. py:module:: pyre.components.Tracker


Module Contents
---------------

.. py:class:: Tracker(**kwds)

   Bases: :class:`pyre.components.Monitor.Monitor`

   A class that monitors the traits of a set of components and maintains a record of their values

   .. method:: track(self, component)


      Add the {component} traits to the pile of observables


   .. method:: flush(self, observable, **kwds)


      Handle the notification that the value of {observable} has changed



