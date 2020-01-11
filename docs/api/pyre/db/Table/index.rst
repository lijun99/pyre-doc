:mod:`pyre.db.Table`
====================

.. py:module:: pyre.db.Table


Module Contents
---------------

.. py:class:: Table

   Bases: :class:`pyre.records.record`

   Base class for database table declarations

   .. attribute:: _pyre_primaryKeys
      

      

   .. attribute:: _pyre_uniqueFields
      

      

   .. attribute:: _pyre_foreignKeys
      

      

   .. attribute:: _pyre_constraints
      

      

   .. method:: pyre_primaryKey(cls, reference)
      :classmethod:


      Add {reference} to the tuple of fields that must be marked as primary keys


   .. method:: pyre_unique(cls, reference)
      :classmethod:


      Add {reference} to the tuple of fields that must be marked as unique


   .. method:: pyre_foreignKey(cls, field, foreign)
      :classmethod:


      Mark {field} as a reference to {foreign}


   .. method:: pyre_check(cls, expression)
      :classmethod:


      Add {expression} to the list of my nameless constraints



