:mod:`pyre.xml.Node`
====================

.. py:module:: pyre.xml.Node


Module Contents
---------------

.. py:class:: Node

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



