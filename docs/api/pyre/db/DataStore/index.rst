:mod:`pyre.db.DataStore`
========================

.. py:module:: pyre.db.DataStore


Module Contents
---------------

.. py:class:: DataStore

   Bases: :class:`pyre.protocol`

   Protocol declaration for database managers

   .. method:: attach(self)


      Establish a connection to the data store


   .. method:: detach(self)


      Close a connection to the data store


   .. method:: execute(self, *sql)


      Execute the sequence of SQL statements in {sql} as a single command



