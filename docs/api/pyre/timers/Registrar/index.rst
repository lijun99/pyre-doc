:mod:`pyre.timers.Registrar`
============================

.. py:module:: pyre.timers.Registrar


Module Contents
---------------

.. py:class:: Registrar(**kwds)

   This class maintains the association between names and timers.

   Registrar acts a timer factory: upon the first use of a given timer name, it builds a timer
   and registers it with its internal index. Subsequent requests for timers by the same name
   return the original instance, effectively making timers accessible in non-local ways. See
   the documentation for {pyre.timers} for more information and simple examples.

   .. attribute:: _index
      

      

   .. method:: timer(self, name, **kwds)


      Build and register a new timer under {name}, if this is the first time {name} is
      used. Otherwise, retrieve the named timer



