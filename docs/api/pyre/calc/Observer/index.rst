:mod:`pyre.calc.Observer`
=========================

.. py:module:: pyre.calc.Observer


Module Contents
---------------

.. py:class:: Observer

   Bases: :class:`pyre.calc.Reactor.Reactor`

   Mix-in class that enables a node to be notified when the value of its dependents change

   .. method:: observe(self, observables)


      Add me as an observer to all {observables}


   .. method:: ignore(self, observables)


      Stop observing the {observables}



