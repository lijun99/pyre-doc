:mod:`pyre.xml.Reader`
======================

.. py:module:: pyre.xml.Reader


Module Contents
---------------

.. py:class:: Reader

   Bases: :class:`xml.sax.ContentHandler`

   An event driver reader for XML documents

   .. attribute:: ignoreWhitespace
      :annotation: = False

      

   .. method:: read(self, *, stream, document, features=(), saxparser=None)


      Build a representation of the information in {stream}

      parameters:
          {stream}: a URI or file-like object
          {document}: an instance of the Document data structure to be decorated with the
                      contents of {stream}
          {saxparser}: the SAX style parser to use; defaults to xml.sax.make_parser()
          {features}: the optional parsing features to enable; expected to be a tuple of
                      (feature, value) pairs; for more details, see the built in package
                      xml.sax or your parser's documentation

      The {Reader} attempts to normalize the exceptions generated while parsing the XML
      document by converting them to one of the exception classes in this package. This
      mechanism fails if you supply your own parser, so you must be ready to catch any
      exceptions it may generate.


   .. method:: startDocument(self)


      Handler for the beginning of the document


   .. method:: startElement(self, name, attributes)


      Handler for the beginning of an element


   .. method:: startElementNS(self, name, qname, attributes)


      Handler for the beginning of an element when feature_namespaces is turned on and the
      element encountered has a namespace qualification, either explicitly given with the
      tag, or because the document specifies a default namespace


   .. method:: characters(self, content)


      Handler for the content of a tag


   .. method:: endElement(self, name)


      Handler for the end of an element


   .. method:: endElementNS(self, name, qname)


      Handler for the end of a namespace qualified element

      Currently there is no known reason to process this differently from normal elements,
      since the reader already knows how to get hold of the responsible handler for this
      event


   .. method:: endDocument(self)


      Handler for the end of the document



