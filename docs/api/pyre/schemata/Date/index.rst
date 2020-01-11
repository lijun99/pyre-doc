:mod:`pyre.schemata.Date`
=========================

.. py:module:: pyre.schemata.Date


Module Contents
---------------

.. py:class:: Date(default=datetime.date.today(), format=format, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for dates

   .. attribute:: format
      :annotation: = %Y-%m-%d

      

   .. attribute:: typename
      :annotation: = date

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a date


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



