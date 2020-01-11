:mod:`pyre.records.CSV`
=======================

.. py:module:: pyre.records.CSV


Module Contents
---------------

.. py:class:: CSV

   A reader and writer of records in csv format

   This class enhances the support provided by the csv package from the python standard
   library by reading and writing records that have a variety of metadata attached to their
   fields, which enables much smarter processing of the information content.

   .. method:: immutable(self, layout, uri=None, stream=None, **kwds)


      Build mutable record instances from a csv formatted source


   .. method:: mutable(self, layout, uri=None, stream=None, **kwds)


      Build mutable record instances from a csv formatted source


   .. method:: read(self, layout, uri=None, stream=None, **kwds)


      Read lines from a csv formatted input source

      The argument {layout} is expected to be a subclass of {pyre.records.Record}. It will be
      inspected to extract the names of the columns to ingest.

      If {uri} is not None, it will be opened for reading in the manner recommended by the
      {csv} package; if {stream} is given instead, it will be passed directly to the {csv}
      package. The first record is assumed to be headers that name the columns of the data.


   .. method:: write(self, sheet, uri=None, stream=None, **kwds)


      Read lines from a csv formatted input source

      The argument {sheet} is expected to be a subclass of {pyre.records.Record}. It will be
      inspected to extract the names of the columns to save.

      If {uri} is not None, it will be opened for writing in the manner recommended by the
      {csv} package; if {stream} is given instead, it will be passed directly to the {csv}
      package



