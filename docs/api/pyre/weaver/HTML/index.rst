:mod:`pyre.weaver.HTML`
=======================

.. py:module:: pyre.weaver.HTML


Module Contents
---------------

.. py:class:: HTML

   Bases: :class:`pyre.weaver.BlockMill.BlockMill`

   Support for HTML

   .. attribute:: doctype
      

      

   .. attribute:: doc
      :annotation: = the doctype variant to use on the first line

      

   .. attribute:: doctypes
      

      

   .. attribute:: startBlock
      :annotation: = <!--

      

   .. attribute:: commentMarker
      :annotation: =  !

      

   .. attribute:: endBlock
      :annotation: = -->

      

   .. method:: header(self)


      Layout the {document} using my stationery for the header


   .. method:: body(self, document=(), **kwds)


      The body of the document


   .. method:: footer(self)


      Layout the {document} using my stationery for the footer



