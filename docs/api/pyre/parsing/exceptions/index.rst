:mod:`pyre.parsing.exceptions`
==============================

.. py:module:: pyre.parsing.exceptions

.. autoapi-nested-parse::

   Definitions for the exceptions raised by this package



Module Contents
---------------

.. py:exception:: ParsingError

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Base class for parsing exceptions

   Can be used to catch all exceptions raised by this package


.. py:exception:: IndentationError

   Bases: :class:`pyre.parsing.exceptions.ParsingError`

   Exception raised when the scanner detects an inconsistent indentation pattern in the source

   .. attribute:: description
      :annotation: = bad indentation

      


.. py:exception:: SyntaxError(token, **kwds)

   Bases: :class:`pyre.parsing.exceptions.ParsingError`

   Exception raised when a syntax error is detected

   .. attribute:: description
      :annotation: = syntax error: {0.token.lexeme!r}

      


.. py:exception:: TokenizationError(text, **kwds)

   Bases: :class:`pyre.parsing.exceptions.ParsingError`

   Exception raised when the scanner fails to extract a token from the input stream

   .. attribute:: description
      :annotation: = could not match {0.text!r}

      


