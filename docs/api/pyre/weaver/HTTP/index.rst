:mod:`pyre.weaver.HTTP`
=======================

.. py:module:: pyre.weaver.HTTP


Module Contents
---------------

.. py:class:: HTTP

   Bases: :class:`pyre.component`

   An HTTP compliant document renderer

   .. attribute:: encoding
      

      

   .. attribute:: doc
      :annotation: = the encoding for HTTP headers

      

   .. attribute:: version
      :annotation: = [1, 0]

      

   .. method:: render(self, document, **kwds)


      Render the document


   .. method:: header(self, document)


      Render the header of the document


   .. method:: body(self, document, **kwds)


      Render the body of the document


   .. method:: footer(self)


      Render the footer of the document



