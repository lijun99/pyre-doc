:mod:`pyre.tabular.Primary`
===========================

.. py:module:: pyre.tabular.Primary


Module Contents
---------------

.. py:class:: Primary(**kwds)

   Bases: :class:`pyre.tabular.Column.Column`

   A selector that serves a column of primary keys, i.e. a column all of whose vales are
   distinct and can be used as an index into the sheet

   .. method:: refresh(self)


      Rebuild my row map


   .. method:: __getitem__(self, value)


      Retrieve the sheet row that contains {value} in my column


   .. method:: prime(self)


      Build my value index



