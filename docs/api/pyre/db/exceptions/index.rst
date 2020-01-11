:mod:`pyre.db.exceptions`
=========================

.. py:module:: pyre.db.exceptions

.. autoapi-nested-parse::

   Definitions for all the exceptions raised by this package



Module Contents
---------------

.. py:exception:: Warning

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Exception raised for important warnings, such as data truncation, loss of precision and
   other idications that the implementation engines have carried out a request in a perhaps
   incorrect way


.. py:exception:: Error

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Base class for all exceptions that are raised by this module to indicate an unrecoverable
   error


.. py:exception:: InterfaceError

   Bases: :class:`pyre.db.exceptions.Error`

   Base class for exceptions raised by the database client code, not the database back end


.. py:exception:: DatabaseError

   Bases: :class:`pyre.db.exceptions.Error`

   Base class for exceptions raised by the database back end


.. py:exception:: DataError

   Bases: :class:`pyre.db.exceptions.DatabaseError`

   Exception raised when a data processing error occurs


.. py:exception:: OperationalError

   Bases: :class:`pyre.db.exceptions.DatabaseError`

   An exception that indicates environmental problems that are generally not related to the
   program itself


.. py:exception:: IntegrityError

   Bases: :class:`pyre.db.exceptions.DatabaseError`

   Exception raised when an operation violates the referential integrity of the data store


.. py:exception:: InternalError

   Bases: :class:`pyre.db.exceptions.DatabaseError`

   Exception raised when the back end reports an internal error


.. py:exception:: ProgrammingError(command, diagnostic, **kwds)

   Bases: :class:`pyre.db.exceptions.DatabaseError`

   Exception raised when there is a problem with the SQL statement being executed

   .. attribute:: description
      :annotation: = while executing {0.command!r}: {0.diagnostic}

      


.. py:exception:: NotSupportedError

   Bases: :class:`pyre.db.exceptions.DatabaseError`

   Exception raised when a method or database API was used that is not supported by the
   database client


