:mod:`pyre.calc.Observable`
===========================

.. py:module:: pyre.calc.Observable


Module Contents
---------------

.. py:class:: Observable(**kwds)

   Bases: :class:`pyre.calc.Reactor.Reactor`

   Mix-in class that notifies its clients when the value of a node changes

   .. method:: observers(self)
      :property:


      Return an iterable over my live observers


   .. method:: addObserver(self, observer)


      Add {observer} to my pile


   .. method:: removeObserver(self, observer)


      Remove {observer} from my pile


   .. method:: replace(self, obsolete)


      Remove {obsolete} from its upstream graph and assume its responsibilities


   .. method:: flush(self, **kwds)


      Handler of the notification event from one of my observables



