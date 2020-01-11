:mod:`pyre.tabular.Chart`
=========================

.. py:module:: pyre.tabular.Chart


Module Contents
---------------

.. py:class:: Chart(sheet, **kwds)

   The base class for imposing coördinate systems on sheets

   A chart contains the specification of a number of dimensions that enable the categorization
   and analysis of the facts in a sheet. For example, given a sales table that contains
   transaction information that includes date, sku and amount, a chart with these three
   dimensions would simplify answering questions such as "compute the total sales of a given
   sku in a given time period".

   Charts are used by pivot tables as a means of imposing structure on the data and
   precomputing data slices. See {pyre.tabular.Pivot} and the {pyre.tabular.Dimension}
   subclasses for more details.

   .. attribute:: pyre_sheets
      

      

   .. attribute:: pyre_dimensions
      

      

   .. attribute:: pyre_localDimensions
      

      

   .. method:: pyre_filter(self, **kwds)


      Create an iterable over those facts that statisfy the criteria specified in {kwds},
      which is assumed to be a value specification for each dimension that is to be used to
      restrict the data set



