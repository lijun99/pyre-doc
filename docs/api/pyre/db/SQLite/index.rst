:mod:`pyre.db.SQLite`
=====================

.. py:module:: pyre.db.SQLite


Module Contents
---------------

.. py:class:: SQLite

   Bases: :class:`pyre.db.Server.Server`

   Component that manages the connection to a sqlite database

   .. attribute:: providesHeaders
      :annotation: = False

      

   .. attribute:: database
      

      

   .. attribute:: doc
      :annotation: = the path to the sqlite database

      

   .. attribute:: cursor
      

      

   .. attribute:: connection
      

      

   .. method:: attach(self)


      Connect to the database


   .. method:: detach(self)


      Close the connection to the database


   .. method:: execute(self, *sql)


      Execute the sequence of SQL statements in {sql} as a single command



