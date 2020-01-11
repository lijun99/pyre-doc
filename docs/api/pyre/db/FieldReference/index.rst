:mod:`pyre.db.FieldReference`
=============================

.. py:module:: pyre.db.FieldReference


Module Contents
---------------

.. py:class:: FieldReference(table, field, **kwds)

   Bases: :class:`pyre.descriptors.stem.variable`

   A field decorator that encapsulates references to table fields

   This class is endowed with the full algebra from {pyre.algebraic} in order to support
   expressions involving table fields. Such expressions can be used to formulate constraints
   or to specify fields in views

   .. attribute:: table
      

      

   .. attribute:: field
      

      

   .. method:: coerce(self, **kwds)


      Convert {value} into my type


   .. method:: project(self, table)


      Build a reference to the given {table} that points to the same field as i do


   .. method:: sql(self, context=None)


      Convert me into an SQL expression



