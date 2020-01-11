:mod:`pyre.http.documents`
==========================

.. py:module:: pyre.http.documents


Module Contents
---------------

.. py:exception:: OK

   Bases: :class:`pyre.http.Response.Response`

   OK

   .. attribute:: code
      :annotation: = 200

      

   .. attribute:: status
      

      

   .. attribute:: description
      :annotation: = Request fulfilled, document follows

      

   .. method:: render(self, **kwds)


      Generate the payload



.. py:exception:: Literal(value, **kwds)

   Bases: :class:`pyre.http.documents.OK`

   A response built out of a literal string

   .. attribute:: encoding
      :annotation: = utf-8

      

   .. method:: render(self, server, **kwds)


      Pack the contents of the file into a binary buffer



.. py:exception:: JSON(value, **kwds)

   Bases: :class:`pyre.http.documents.OK`

   A response built out of the JSON encoding of a python object

   .. attribute:: encoding
      :annotation: = utf-8

      

   .. method:: render(self, **kwds)


      Encode the object in JSON format



.. py:exception:: Document(application, **kwds)

   Bases: :class:`pyre.http.documents.OK`

   A response built out of an application generated document


.. py:exception:: File(uri, **kwds)

   Bases: :class:`pyre.http.documents.Document`

   A document response built out of a file in the application private document root

   .. attribute:: uri
      

      

   .. method:: render(self, server, **kwds)


      Pack the contents of the file into a binary buffer



