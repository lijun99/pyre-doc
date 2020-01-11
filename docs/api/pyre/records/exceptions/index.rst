:mod:`pyre.records.exceptions`
==============================

.. py:module:: pyre.records.exceptions

.. autoapi-nested-parse::

   Definitions for all the exceptions raised by this package



Module Contents
---------------

.. py:exception:: RecordError

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   The base class of all exceptions raised by this package


.. py:exception:: SourceSpecificationError

   Bases: :class:`pyre.records.exceptions.RecordError`

   A method that reads records from external input sources was given an invalid input
   specification

   .. attribute:: description
      :annotation: = invalid input source specification

      


