:mod:`pyre.schemata.Time`
=========================

.. py:module:: pyre.schemata.Time


Module Contents
---------------

.. py:class:: Time(default=datetime.datetime.today(), format=format, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for timestamps

   .. attribute:: format
      :annotation: = %H:%M:%S

      

   .. attribute:: typename
      :annotation: = time

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a time

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a timestamp


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



