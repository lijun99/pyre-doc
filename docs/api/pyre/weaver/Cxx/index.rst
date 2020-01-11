:mod:`pyre.weaver.Cxx`
======================

.. py:module:: pyre.weaver.Cxx


Module Contents
---------------

.. py:class:: Cxx(**kwds)

   Bases: :class:`pyre.weaver.LineMill.LineMill`, :class:`pyre.weaver.Expression.Expression`

   Support for C++

   .. attribute:: languageMarker
      

      

   .. attribute:: doc
      :annotation: = the variant to use in the language marker

      

   .. attribute:: comment
      :annotation: = //

      

   .. method:: _powerRenderer(self, node)


      Render {node.op1} raised to the {node.op2} power



