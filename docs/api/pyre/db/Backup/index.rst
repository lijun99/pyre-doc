:mod:`pyre.db.Backup`
=====================

.. py:module:: pyre.db.Backup


Module Contents
---------------

.. py:class:: Backup

   Bases: :class:`pyre.db.Server.Server`

   Component that saves SQL statement in a stream

   .. attribute:: database
      

      

   .. attribute:: doc
      :annotation: = the name of the database to connect to

      

   .. attribute:: stream
      

      

   .. attribute:: doc
      :annotation: = the stream in which to place SQL statements

      

   .. method:: attach(self)


      Connect to the database


   .. method:: detach(self)


      Close the connection to the database


   .. method:: execute(self, *sql)


      Execute the sequence of SQL statements in {sql} as a single command


   .. method:: __enter__(self)


      Hook invoked when the context manager is entered


   .. method:: __exit__(self, exc_type, exc_instance, exc_traceback)


      Hook invoked when the context manager's block exits



