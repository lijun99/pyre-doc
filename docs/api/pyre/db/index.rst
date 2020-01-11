:mod:`pyre.db`
==============

.. py:module:: pyre.db

.. autoapi-nested-parse::

   Machinery for building connections to database back ends



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Backup/index.rst
   Client/index.rst
   Collation/index.rst
   DataStore/index.rst
   FieldReference/index.rst
   FieldSelector/index.rst
   ForeignKey/index.rst
   Measure/index.rst
   Object/index.rst
   Persistent/index.rst
   Postgres/index.rst
   Query/index.rst
   Reference/index.rst
   SQL/index.rst
   SQLite/index.rst
   Schemer/index.rst
   Selector/index.rst
   Server/index.rst
   Table/index.rst
   actions/index.rst
   exceptions/index.rst
   expressions/index.rst
   literals/index.rst


Package Contents
----------------

.. data:: null
   

   

.. data:: default
   

   

.. data:: noAction
   :annotation: = NO ACTION

   

.. data:: restrict
   :annotation: = RESTRICT

   

.. data:: cascade
   :annotation: = CASCADE

   

.. data:: setNull
   :annotation: = SET NULL

   

.. data:: setDefault
   :annotation: = SET DEFAULT

   

.. py:class:: collation(fieldref, collation=collation, **kwds)

   An encapsulation of the collation sequence

   .. attribute:: fieldref
      

      

   .. attribute:: collation
      :annotation: = ASC

      

   .. method:: sql(self, context=None)


      Render me as an SQL expression



.. function:: ascending(fieldref)

   Build a clause for the {ORDER} expression that marks {fieldref} as sorted in ascending
   order


.. function:: descending(fieldref)

   Build a clause for the {ORDER} expression that marks {fieldref} as sorted in descending
   order


.. py:class:: isNull

   Bases: :class:`pyre.db.expressions.UnaryPostfix`

   A node factory that takes a field reference {op} and builds the expression {op IS NULL}

   .. attribute:: operator
      :annotation: = IS NULL

      


.. py:class:: isNotNull

   Bases: :class:`pyre.db.expressions.UnaryPostfix`

   A node factory that takes a field reference {op} and builds the expression {op IS NOT NULL}

   .. attribute:: operator
      :annotation: = IS NOT NULL

      


.. py:class:: cast(field, targetType, **kwds)

   Implementation of the {CAST} expression

   .. method:: sql(self, **kwds)


      SQL rendering of the expression I represent



.. py:class:: like(field, regex, **kwds)

   Implementation of the LIKE operator

   .. method:: sql(self, **kwds)


      SQL rendering of the expression I represent



.. data:: field
   

   

.. py:class:: measure

   Bases: :class:`pyre.records.measure`

   The base class for table field descriptors

   .. py:class:: measure

      The base class of the local mixins.

      Its purpose is to trap value coercion and skip it for the special values {NULL} and
      {DEFAULT} that show up as {literals} instances

      .. method:: coerce(self, value, **kwds)




   .. py:class:: bool

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for booleans

      .. attribute:: decl
         :annotation: = BOOLEAN

         

      .. method:: sql(self, value)


         SQL rendering of {value}



   .. py:class:: date(default=None, **kwds)

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for dates

      .. attribute:: decl
         :annotation: = DATE

         

      .. method:: sql(self, value)


         SQL rendering of {value}



   .. py:class:: decimal(precision, scale, **kwds)

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for fixed point numbers

      .. method:: decl(self)
         :property:


         SQL rendering of my type name


      .. method:: sql(self, value)


         SQL rendering of {value}



   .. py:class:: float

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for floating point numbers

      .. attribute:: decl
         :annotation: = DOUBLE PRECISION

         

      .. method:: sql(self, value)


         SQL rendering of my value



   .. py:class:: int

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for integers

      .. attribute:: decl
         :annotation: = INTEGER

         

      .. method:: sql(self, value)


         SQL rendering of my value



   .. py:class:: str(maxlen=None, **kwds)

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for strings

      .. method:: decl(self)
         :property:


         SQL rendering of my type name


      .. method:: sql(self, value)


         SQL rendering of my value



   .. py:class:: time(default=None, timezone=False, **kwds)

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for timestamps

      .. method:: decl(self)
         :property:


         SQL rendering of my type name


      .. method:: sql(self, value)


         SQL rendering of {value}



   .. attribute:: _primary
      

      

   .. attribute:: _unique
      

      

   .. attribute:: _notNull
      

      

   .. attribute:: _foreign
      

      

   .. method:: setDefault(self, value)


      Set a new default value


   .. method:: primary(self)


      Mark a field as a primary key


   .. method:: unique(self)


      Mark a field as containing values that are unique across the table rows


   .. method:: notNull(self)


      Mark a field as not accepting a NULL value


   .. method:: references(self, **kwds)


      Mark a field as a foreign key


   .. method:: decldefault(self)


      Invoked by the SQL mill to create the declaration of the default value



.. data:: bool
   

   

.. data:: date
   

   

.. data:: decimal
   

   

.. data:: float
   

   

.. data:: int
   

   

.. data:: str
   

   

.. data:: time
   

   

.. py:class:: reference(**kwds)

   Bases: :class:`pyre.db.Measure.Measure`

   Representation of foreign keys

   .. method:: decl(self)
      :property:


      SQL rendering of my type name


   .. method:: sql(self, value)


      SQL rendering of {value}


   .. method:: onDelete(self, action)


      Set the action to perform when the target record is deleted. See {pyre.db.actions} for
      details


   .. method:: onUpdate(self, action)


      Set the action to perform when the target record is updated. See {pyre.db.actions} for
      details



.. py:class:: table

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



.. py:class:: query

   Bases: :class:`pyre.records.record`

   Base class for describing database queries

   .. attribute:: where
      

      

   .. attribute:: order
      

      

   .. attribute:: group
      

      

   .. attribute:: pyre_tables
      

      


.. py:class:: object

   Bases: :class:`pyre.framework.Dashboard.Dashboard`

   The base class of classes whose instances store part of their attributes in relational
   database tables.

   {Object} and its class {Persistent} provide the necessary layer to bridge object oriented
   semantics with the relational model. The goal is to make the existence of the relational
   tables more transparent to the developer of database applications by removing as much of
   the grunt work of storing and retrieving object state as possible.

   .. attribute:: pyre_extent
      

      

   .. attribute:: pyre_primaryTable
      

      


.. py:class:: datastore

   Bases: :class:`pyre.protocol`

   Protocol declaration for database managers

   .. method:: attach(self)


      Establish a connection to the data store


   .. method:: detach(self)


      Close a connection to the data store


   .. method:: execute(self, *sql)


      Execute the sequence of SQL statements in {sql} as a single command



.. py:class:: sql(**kwds)

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



.. py:class:: server

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



.. py:class:: client

   Bases: :class:`pyre.component`

   The base class for components that connect to data stores

   .. attribute:: server
      

      


.. py:class:: backup

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



.. py:class:: sqlite

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



.. py:class:: postgres

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




.. function:: template(table)

   Build a row of {table} with all its fields set to {None}.


