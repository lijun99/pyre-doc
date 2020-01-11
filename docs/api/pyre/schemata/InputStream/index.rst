:mod:`pyre.schemata.InputStream`
================================

.. py:module:: pyre.schemata.InputStream


Module Contents
---------------

.. py:class:: InputStream(default='stdin', mode=mode, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`, :class:`pyre.framework.Dashboard.Dashboard`

   A representation of input streams

   .. attribute:: mode
      :annotation: = r

      

   .. attribute:: typename
      :annotation: = istream

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into an open input stream


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



