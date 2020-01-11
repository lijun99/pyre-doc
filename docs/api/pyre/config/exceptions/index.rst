:mod:`pyre.config.exceptions`
=============================

.. py:module:: pyre.config.exceptions

.. autoapi-nested-parse::

   Definitions for all the exceptions raised by this package



Module Contents
---------------

.. py:exception:: ConfigurationError

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Base class for all configuration errors


.. py:exception:: CodecError(codec, uri='', **kwds)

   Bases: :class:`pyre.config.exceptions.ConfigurationError`

   Base class for codec errors

   .. attribute:: description
      :annotation: = generic codec error

      


.. py:exception:: UnknownEncodingError(encoding, **kwds)

   Bases: :class:`pyre.config.exceptions.CodecError`

   A request for an unknown codec was made

   .. attribute:: description
      :annotation: = {0.uri.uri!r}: unknown encoding {0.encoding!r}

      


.. py:exception:: DecodingError

   Bases: :class:`pyre.config.exceptions.CodecError`

   Exception raised by codecs when they encounter errors in their input streams


.. py:exception:: EncodingError

   Bases: :class:`pyre.config.exceptions.CodecError`

   Exception raised by codecs when they fail to inject an item in a stream


.. py:exception:: LoadingError

   Bases: :class:`pyre.config.exceptions.CodecError`

   Exception raised by codecs when they encounter errors in their input streams


.. py:exception:: ShelfError(shelf, **kwds)

   Bases: :class:`pyre.config.exceptions.ConfigurationError`


.. py:exception:: SymbolNotFoundError(symbol, **kwds)

   Bases: :class:`pyre.config.exceptions.ShelfError`

   .. attribute:: description
      :annotation: = symbol {0.symbol!r} not found in {0.shelf!r}

      


