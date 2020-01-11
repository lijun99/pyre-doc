:mod:`pyre.xml.exceptions`
==========================

.. py:module:: pyre.xml.exceptions

.. autoapi-nested-parse::

   Definitions for all the exceptions raised by this package



Module Contents
---------------

.. py:exception:: ParsingError(parser=None, document=None, **kwds)

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Base class for parsing errors


.. py:exception:: UnsupportedFeatureError(features, **kwds)

   Bases: :class:`pyre.xml.exceptions.ParsingError`

   Exception raised when one of the requested features is not supported by the parser


.. py:exception:: DTDError

   Bases: :class:`pyre.xml.exceptions.ParsingError`

   Errors relating to the structure of the document


.. py:exception:: ProcessingError(saxlocator, **kwds)

   Bases: :class:`pyre.xml.exceptions.ParsingError`

   Errors relating to the handling of the document

   .. attribute:: description
      :annotation: = unknown processing error

      


