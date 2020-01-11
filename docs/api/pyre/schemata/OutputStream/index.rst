:mod:`pyre.schemata.OutputStream`
=================================

.. py:module:: pyre.schemata.OutputStream


Module Contents
---------------

.. py:class:: OutputStream(default='stdout', mode=mode, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`, :class:`pyre.framework.Dashboard.Dashboard`

   A representation of input streams

   .. attribute:: mode
      :annotation: = w

      

   .. attribute:: typename
      :annotation: = ostream

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into an open input stream


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



