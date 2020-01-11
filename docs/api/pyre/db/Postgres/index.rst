:mod:`pyre.db.Postgres`
=======================

.. py:module:: pyre.db.Postgres


Module Contents
---------------

.. py:class:: Postgres

   Bases: :class:`pyre.db.Server.Server`

   Component that manages the connection to a Postgres database

   .. attribute:: database
      

      

   .. attribute:: doc
      :annotation: = the name of the database to connect to

      

   .. attribute:: username
      

      

   .. attribute:: doc
      :annotation: = the database user name to use during authentication

      

   .. attribute:: password
      

      

   .. attribute:: doc
      :annotation: = the password of the database user

      

   .. attribute:: application
      

      

   .. attribute:: doc
      :annotation: = the application name to use for the connection

      

   .. attribute:: quiet
      

      

   .. attribute:: doc
      :annotation: = control whether certain postgres informationals are shown

      

   .. attribute:: postgres
      

      

   .. attribute:: connection
      

      

   .. method:: attach(self)


      Connect to the database


   .. method:: detach(self)


      Close the connection to the database

      Closing a connection makes it unsuitable for any further database access. This applies
      to all objects that may retain a reference to the connection being closed. Any
      uncommitted changes will be lost


   .. method:: execute(self, *sql)


      Execute the sequence of SQL statements in {sql} as a single command


   .. method:: __enter__(self)


      Hook invoked when the context manager is entered


   .. method:: __exit__(self, exc_type, exc_instance, exc_traceback)


      Hook invoked when the context manager's block exits


   .. method:: initializeExtension(cls)
      :classmethod:




