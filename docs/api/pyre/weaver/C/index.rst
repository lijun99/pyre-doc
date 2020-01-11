:mod:`pyre.weaver.C`
====================

.. py:module:: pyre.weaver.C


Module Contents
---------------

.. py:class:: C(**kwds)

   Bases: :class:`pyre.weaver.BlockMill.BlockMill`, :class:`pyre.weaver.Expression.Expression`

   Support for C

   .. attribute:: languageMarker
      

      

   .. attribute:: doc
      :annotation: = the variant to use in the language marker

      

   .. attribute:: startBlock
      :annotation: = /*

      

   .. attribute:: commentMarker
      :annotation: =  *

      

   .. attribute:: endBlock
      :annotation: = */

      

   .. method:: _powerRenderer(self, node)


      Render {node.op1} raised to the {node.op2} power



