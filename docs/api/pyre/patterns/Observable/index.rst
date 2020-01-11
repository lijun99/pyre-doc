:mod:`pyre.patterns.Observable`
===============================

.. py:module:: pyre.patterns.Observable


Module Contents
---------------

.. py:class:: Observable(**kwds)

   Provide notification support for classes that maintain dynamic associations with multiple
   clients.

   Observers, i.e. clients of the Observable, register event handlers that will be invoked to
   notify them whenever something interesting happens to the Observable. The nature of what is
   being observed is defined by Observable descendants and their managers. For example,
   instances of pyre.calc.Node are observable by the other nodes whose value depends on
   them. These dependents are notified of value changes and forced to refresh their value
   cache.

   The event handlers are callables that take the observable instance as their single
   argument.

   interface:
     addObserver: registers its callable argument with the list of handlers to invoke
     removeObserver: remove an event handler from the list of handlers to invoke
     notifyObservers: invoke the registered handlers in the order in which they were registered

   .. attribute:: observers
      

      

   .. method:: notifyObservers(self, **kwds)


      Notify all observers


   .. method:: addObserver(self, callback)


      Add {callback} to the set of observers


   .. method:: removeObserver(self, callback)


      Remove {callback} from the set of observers



