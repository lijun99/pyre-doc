:mod:`pyre.weaver.Mill`
=======================

.. py:module:: pyre.weaver.Mill


Module Contents
---------------

.. py:class:: Mill

   Bases: :class:`pyre.component`, :class:`pyre.weaver.Indenter.Indenter`

   The base class for text renderers

   .. attribute:: stationery
      

      

   .. attribute:: doc
      :annotation: = the overall layout of the document

      

   .. attribute:: languageMarker
      

      

   .. attribute:: doc
      :annotation: = the string to use as the language marker

      

   .. method:: render(self, **kwds)


      Layout the {document} using my stationery for the header and footer


   .. method:: header(self)


      Build the header of the document


   .. method:: body(self, document=())


      The body of the document


   .. method:: footer(self)


      Build the footer of the document


   .. method:: _header(self)


      Workhorse for the header generator



