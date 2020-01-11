:mod:`pyre.http.exceptions`
===========================

.. py:module:: pyre.http.exceptions


Module Contents
---------------

.. py:exception:: ProtocolError(**kwds)

   Bases: :class:`pyre.http.Response.Response`

   Base exceptions for all error conditions detected by http components

   .. method:: render(self, **kwds)


      Create a representation of the error suitable for transporting to the user agent


   .. method:: __str__(self)


      The default rendering of protocol errors



