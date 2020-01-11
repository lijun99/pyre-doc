:mod:`pyre.flow.Status`
=======================

.. py:module:: pyre.flow.Status


Module Contents
---------------

.. py:class:: Status(node, raw=raw, **kwds)

   Bases: :class:`pyre.tracker`

   A helper that watches over a component's traits and records value changes

   .. attribute:: raw
      :annotation: = True

      

   .. method:: track(self)


      Start tracking my {node}


   .. method:: flush(self, observable, **kwds)


      Handler of the notification that the value of {observable} has changed



