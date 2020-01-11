:mod:`pyre.framework.exceptions`
================================

.. py:module:: pyre.framework.exceptions


Module Contents
---------------

.. py:exception:: PyreError(description=None, locator=None, **kwds)

   Bases: :class:`Exception`

   Base class for all pyre related errors

   .. attribute:: description
      :annotation: = generic pyre error

      

   .. method:: __str__(self)




.. py:exception:: FrameworkError

   Bases: :class:`pyre.framework.exceptions.PyreError`

   Base class for all framework exceptions

   Useful when you are trying to catch any and all pyre framework errors


.. py:exception:: BadResourceLocatorError(uri, reason, **kwds)

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Exception raised when a URI is not formed properly

   .. attribute:: description
      :annotation: = {0.uri}: {0.reason}

      


.. py:exception:: ComponentNotFoundError(uri, **kwds)

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   .. attribute:: description
      :annotation: = could not resolve {0.uri} into a component

      


.. py:exception:: ExternalNotFoundError(category, **kwds)

   Bases: :class:`pyre.framework.exceptions.FrameworkError`

   Base class for parsing errors

   .. attribute:: description
      :annotation: = could not locate support for external package {0.category!r}

      


