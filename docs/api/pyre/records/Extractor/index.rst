:mod:`pyre.records.Extractor`
=============================

.. py:module:: pyre.records.Extractor


Module Contents
---------------

.. py:class:: Extractor

   A strategy for pulling data from a stream and performing value coercions indicated by the
   field descriptors

   .. method:: __call__(self, record, source, **kwds)


      Pull values from {source}, convert and yield them



