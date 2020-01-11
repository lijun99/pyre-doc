:mod:`pyre.weaver.SQL`
======================

.. py:module:: pyre.weaver.SQL


Module Contents
---------------

.. py:class:: SQL(**kwds)

   Bases: :class:`pyre.weaver.LineMill.LineMill`, :class:`pyre.weaver.Expression.Expression`

   Support for SQL

   .. attribute:: languageMarker
      

      

   .. attribute:: doc
      :annotation: = the variant to use in the language marker

      

   .. attribute:: comment
      :annotation: = --

      

   .. method:: _literalRenderer(self, node, **kwds)


      Render {node} as a literal



