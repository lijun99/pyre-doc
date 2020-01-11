:mod:`pyre.xml.Document`
========================

.. py:module:: pyre.xml.Document


Module Contents
---------------

.. py:class:: Document

   Bases: :class:`pyre.xml.Node.Node`

   Base class for the custom processing of XML parsing events. You must derive from this class
   and declare the element descriptors that correspond to the tags in your document.
   Instances of your derived class will form the interface between the XML parser and the
   application specific data structure being decorated with the contents of the XML stream.

   This object is the anchor for the handler of the top element handler that is reposinsible
   for the root of the XML document.

   The DTD metaclass scans through the class record, identifies the element declarations and
   builds the DTF for the document

   .. attribute:: tag
      :annotation: = document

      

   .. attribute:: root
      

      

   .. attribute:: elements
      :annotation: = []

      

   .. attribute:: dtd
      

      

   .. attribute:: dom
      

      

   .. attribute:: _pyre_nodeIndex
      

      

   .. method:: initialize(self, locator)


      Handler for the event generated when parsing the XML document has just begun


   .. method:: finalize(self, locator)


      Handler for the event generated when parsing of the XML document is finished



