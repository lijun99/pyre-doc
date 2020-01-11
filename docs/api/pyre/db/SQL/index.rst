:mod:`pyre.db.SQL`
==================

.. py:module:: pyre.db.SQL


Module Contents
---------------

.. py:class:: SQL(**kwds)

   Bases: :class:`pyre.weaver.SQL.SQL`

   Generate SQL statements

   .. attribute:: INDENTER
      

      

   .. method:: select(self, query)


      Generate the SELECT statement described by {query}


   .. method:: transaction(self)


      Generate the SQL statement that initiates a transaction block


   .. method:: commit(self)


      Generate the SQL statement that closes a transaction block


   .. method:: rollback(self)


      Generate the SQL statement that rolls back a transaction


   .. method:: createDatabase(self, name)


      Generate the SQL statement to create the database {name}


   .. method:: dropDatabase(self, name)


      Generate the SQL statement to drop the database {name}


   .. method:: createTable(self, table)


      Generate the SQL statement to create a database table given its description

      The {table} specification is expected to be a {Table} subclass, with the necessary
      column information provided by the decorated field descriptors


   .. method:: dropTable(self, table)


      Build the statement to drop the given {table}


   .. method:: insertRecords(self, *records)


      Insert {records}, an iterable of table records, into their corresponding table


   .. method:: deleteRecords(self, table, condition)


      Remove all {table} records that match {condition}

      If condition is {None}, this routine will remove all records from the given {table}


   .. method:: updateRecords(self, template, condition)


      Update all table rows that match {condition} using information from {template}, a
      prototype row of a table. The update operation sets the fields in these rows to their
      corresponding values in {template}; fields set to {None} in {template} are not
      affected.


   .. method:: _collationRenderer(self, order, context=None, **kwds)


      Render the collation order specification


   .. method:: _fieldReferenceRenderer(self, node, context=None, **kwds)


      Render {node} as reference to a field


   .. method:: _primitiveSQLExpressionRenderer(self, node, context=None, **kwds)


      Render {node} as a unary postfix operator


   .. method:: _fieldDeclaration(self, field, comma)


      Build the declaration lines for a given table field


   .. method:: _referenceDeclaration(self, foreign, comma)


      Build a declaration for a foreign key



