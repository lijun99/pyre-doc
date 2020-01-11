:mod:`pyre.xml`
===============

.. py:module:: pyre.xml

.. autoapi-nested-parse::

   This package contains the machinery to build parsers of XML documents

   The goal of this package is to enable context-specific processing of the information content of
   the XML file. It is designed to provide support for applications that use XML files as an
   information exchange mechanism and consider parsing the XML file as another means for
   decorating their data structures.

   There are two styles of processing the contents of XML files in common use that go by the names
   DOM and SAX. DOM processing is generally considered to be the simplest way. It constructs a
   representation of the entire file with a single function call to the parser and returns a data
   structure that has a very faithful representation of the layout of the file, along with a rich
   interface for navigating through the representation and discovering its content. In contrast,
   SAX parsing is event driven. The parser scans through the document and generates events for
   each significant encounter with the document contents, such the opening or closing of an XML
   tag, or encountering data in the body of a tag. The client interacts with the parser by
   registering handlers for each type of event that are responsible for absorbing the information
   collected by te parser. This trades some complexity in the handling of the document for the
   savings of not needing to build and subsequently navigate through an intermediate data
   structure.

   Overall, SAX style document parsing should be faster and more space efficient for most uses. It
   also opens up the possibility that an application can implement its event handlers in a way that
   directly decorate its own internal data structures. The purpose of this package is to help
   minimize the code complexity required to craft event handlers and register them with the
   parser.

   As a prototypical example, consider an address book application that maintains contact
   information for friends and clients. Such an application is likely to have a rather extensive
   set of classes that handle the various type of contacts and their associated information. The
   addressbook is likely some type of container of such classes. Support for retrieving contact
   information from XML files ideally should be just another way to construct the application
   specific data structures and adding them to the addressbook container. The application
   developer should be shielded as much as possible from the mechanics of parsing XML files and
   the intermediate data structures necessary to store the file contents.

   The application in the examples directory is a trivial implementation of an addressbook but
   highlights all the important steps for creating handlers/decorators for converting XML files
   into live data structures.



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   AttributeDescriptor/index.rst
   DTD/index.rst
   Descriptor/index.rst
   Document/index.rst
   ElementDescriptor/index.rst
   Ignorable/index.rst
   Node/index.rst
   Reader/index.rst
   exceptions/index.rst


Package Contents
----------------

.. function:: newReader(**kwds)

   Create a new reader


.. function:: newLocator(saxlocator)

   Convert a locator from the SAX parser to a pyre.tracking.FileLocator


.. py:class:: node

   The base class for parsing event handlers

   .. attribute:: tag
      

      

   .. attribute:: elements
      :annotation: = []

      

   .. attribute:: namespace
      :annotation: = 

      

   .. attribute:: newLocator
      

      

   .. attribute:: _pyre_nodeIndex
      

      

   .. attribute:: _pyre_nodeQIndex
      

      

   .. method:: content(self, text, locator)


      The handler for textual data within my body that is not associated with any of my children


   .. method:: newNode(self, *, name, attributes, locator)


      The handler invoked when the opening tag for one of my children is encountered.

      The default implementation looks up the tag in my local dtd, retrieves the associated
      node factory, and invokes it to set up the context for handlingits content

      In typical use, there is no need to override this; but if you do, you should make sure
      to return a Node descendant that is properly set up to handle the contents of the named
      tag


   .. method:: newQNode(self, *, name, namespace, attributes, locator)


      The handler invoked when the opening tag for one of my namespace qualified children is
      encountered.

      See Node.newNode for details


   .. method:: notify(self, *, parent, locator)
      :abstractmethod:


      The handler that is invoked when the parser encounters my closing tag



.. py:class:: ignorable(**kwds)

   Bases: :class:`pyre.xml.Node.Node`

   Handler that ignores the subtree anchored at its tag

   .. method:: newNode(self, **kwds)


      Invoked when a new opening tag is encountered in my subtree


   .. method:: newQNode(self, **kwds)


      Invoked when a new namespace qualified opening tag is encountered in my subtree


   .. method:: notify(self, **kwds)


      Invoked when a closing tag in encountered in my subtree



.. py:class:: document

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



.. py:class:: element(*, tag, handler, root=False)

   Bases: :class:`pyre.xml.Descriptor.Descriptor`

   Descriptor class that gathers all the metadata about a document tag that was provided by
   the user during the DTD declaration. It is used by DTD derived classes to decorate the
   Document instance and the tag handlers with the information needed by the Reader so it can
   process XML documents

   .. attribute:: handler
      

      

   .. attribute:: attributes
      :annotation: = []

      


.. data:: CDATA
   :annotation: = CDATA

   

.. data:: ID
   :annotation: = ID

   

.. data:: IDREFS
   :annotation: = IDREFS

   

.. data:: NMTOKEN
   :annotation: = NMTOKEN

   

.. data:: NMTOKENS
   :annotation: = NMTOKENS

   

.. data:: ENTITY
   :annotation: = ENTITY

   

.. data:: ENTITIES
   :annotation: = ENTITIES

   

.. data:: NOTATION
   :annotation: = NOTATION

   

.. data:: XML
   :annotation: = xml:

   

.. data:: REQUIRED
   :annotation: = #REQUIRED

   

.. data:: IMPLIED
   :annotation: = #IMPLIED

   

.. data:: FIXED
   :annotation: = #FIXED

   

