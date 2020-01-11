:mod:`pyre.db.Server`
=====================

.. py:module:: pyre.db.Server


Module Contents
---------------

.. py:class:: Server

   Bases: :class:`pyre.component`

   Abstract component that encapsulates the connection to a database back end

   This class is meant to be used as the base class for back end specific component
   implementations. It provides a complete but trivial implementation of the {DataStore}
   interface.

   .. attribute:: providesHeaders
      :annotation: = True

      

   .. attribute:: sql
      

      

   .. attribute:: doc
      :annotation: = the generator of the SQL statements

      

   .. method:: attach(self)
      :abstractmethod:


      Connect to the database back end


   .. method:: detach(self)
      :abstractmethod:


      Connect to the database back end


   .. method:: execute(self, *sql)
      :abstractmethod:


      Execute the sequence of SQL statements in {sql} as a single command


   .. method:: createDatabase(self, name)


      Build and execute the SQL statement to create the database {name}


   .. method:: dropDatabase(self, name)


      Build and execute the SQL statement to drop the database {name}


   .. method:: createTable(self, table)


      Build and execute the SQL statement necessary to create {table}


   .. method:: dropTable(self, table)


      Build and execute the SQL statement necessary to delete {table} from the datastore


   .. method:: insert(self, *records)


      Insert {records} into the database


   .. method:: update(self, *specifications)


      Use {specifications} to update the database

      Each item in {specifications} is a pair of a {template} and a {condition}. The
      {template} is an instance of a table row with all fields that require update having
      values that are not {None}. The {condition} is an expression that identifies the
      portion of the table that will be affected


   .. method:: delete(self, table, condition)


      Delete all {table} records that match {condition}


   .. method:: select(self, query)


      Execute the given {query} and return the retrieved data


   .. method:: __enter__(self)


      Hook invoked when the context manager is entered


   .. method:: __exit__(self, exc_type, exc_instance, exc_traceback)


      Hook invoked when the context manager's block exits



