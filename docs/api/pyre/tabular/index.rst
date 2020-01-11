:mod:`pyre.tabular`
===================

.. py:module:: pyre.tabular


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Chart/index.rst
   Column/index.rst
   Dimension/index.rst
   Inferred/index.rst
   Interval/index.rst
   Measure/index.rst
   Pivot/index.rst
   Primary/index.rst
   Reduction/index.rst
   Selector/index.rst
   Sheet/index.rst
   Surveyor/index.rst
   Tabulator/index.rst
   View/index.rst
   exceptions/index.rst


Package Contents
----------------

.. data:: field
   

   

.. data:: derivation
   

   

.. data:: literal
   

   

.. py:class:: measure

   Bases: :class:`pyre.records.measure`

   Base class for the measures in this package

   .. attribute:: _primary
      :annotation: = False

      

   .. method:: primary(self)


      Mark this measure as a primary key



.. data:: bool
   

   

.. data:: decimal
   

   

.. data:: float
   

   

.. data:: inet
   

   

.. data:: int
   

   

.. data:: identity
   

   

.. data:: str
   

   

.. data:: date
   

   

.. data:: dimensional
   

   

.. data:: time
   

   

.. data:: uri
   

   

.. data:: list
   

   

.. data:: set
   

   

.. data:: tuple
   

   

.. py:class:: sheet(name, **kwds)

   Bases: :class:`pyre.records.record`

   The base class for pyre worksheets, collections of record instances

   .. attribute:: pyre_name
      

      

   .. attribute:: pyre_data
      

      

   .. method:: pyre_immutable(self, data)


      Iterate over {data} extracting records that are compatible with my layout and use them to
      populate my data set


   .. method:: pyre_mutable(self, data)


      Iterate over {data} extracting records that are compatible with my layout and use them to
      populate my data set


   .. method:: pyre_append(self, row)


      Add the given {row} to my data set


   .. method:: pyre_new(self)


      Create a new blank mutable record instance and add it to my data set


   .. method:: pyre_offset(cls, measure)
      :classmethod:


      Return the column number of {measure}


   .. method:: __len__(self)


      Compute the number of records in my dataset


   .. method:: __iter__(self)


      Build an iterator over my data set


   .. method:: __getitem__(self, address)


      Retrieve the portion of the sheet that corresponds to {address}



.. py:class:: inferred

   Bases: :class:`pyre.tabular.Dimension.Dimension`

   A chart axis whose tick marks are the unique values found in a given sheet column

   .. py:class:: axis(chart, dimension, **kwds)

      Bases: :class:`dict`


   .. method:: __get__(self, chart, cls)




.. py:class:: interval(interval, subdivisions, **kwds)

   Bases: :class:`pyre.tabular.Dimension.Dimension`

   A chart axis whose tick marks are intervals of (a subset) of the range of the values in a
   given sheet column.

   .. py:class:: axis(chart, dimension, **kwds)

      .. method:: __len__(self)



      .. method:: __iter__(self)



      .. method:: __getitem__(self, bin)




   .. method:: __get__(self, chart, cls)




.. py:class:: chart(sheet, **kwds)

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



.. data:: record
   

   

.. data:: csv
   

   

.. py:class:: tabulator

   Bases: :class:`pyre.records.templater`

   Metaclass that builds sheets


.. py:class:: surveyor

   Bases: :class:`pyre.patterns.AttributeClassifier.AttributeClassifier`

   Inspect charts and harvest their dimensions

   .. method:: __prepare__(cls, name, bases, **kwds)
      :classmethod:


      Prepare a container for the attributes of a chart by looking through {kwds} for sheet
      aliases and making them available as class attributes during the chart
      declaration. This makes it possible to refer to sheets when setting up the chart
      dimensions



