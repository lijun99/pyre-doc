:mod:`pyre.weaver.XML`
======================

.. py:module:: pyre.weaver.XML


Module Contents
---------------

.. py:class:: XML(**kwds)

   Bases: :class:`pyre.weaver.BlockMill.BlockMill`

   Support for XML

   .. attribute:: startBlock
      :annotation: = <!--

      

   .. attribute:: commentMarker
      :annotation: =  !

      

   .. attribute:: endBlock
      :annotation: = -->

      

   .. method:: header(self)


      Layout the {document} using my stationery for the header and footer


   .. method:: push(self, tag, attributes=None)


      Open a {tag}


   .. method:: pop(self)


      Pop a tag from the stack



