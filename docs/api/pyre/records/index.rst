:mod:`pyre.records`
===================

.. py:module:: pyre.records


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Accessor/index.rst
   CSV/index.rst
   Calculator/index.rst
   Compiler/index.rst
   Evaluator/index.rst
   Extractor/index.rst
   Immutable/index.rst
   Mutable/index.rst
   NamedTuple/index.rst
   Record/index.rst
   Selector/index.rst
   Templater/index.rst
   exceptions/index.rst


Package Contents
----------------

.. data:: field
   

   

.. data:: measure
   

   

.. data:: derivation
   

   

.. data:: literal
   

   

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
   

   

.. data:: converter
   

   

.. data:: normalizer
   

   

.. data:: validator
   

   

.. py:class:: selector(index, field, **kwds)

   The base class for objects responsible for providing named access to field descriptors

   .. attribute:: index
      

      

   .. attribute:: field
      

      

   .. method:: __get__(self, record, cls)


      Field retrieval


   .. method:: __set__(self, record, value)
      :abstractmethod:


      Field modification



.. py:class:: templater(name, bases, attributes, **kwds)

   Bases: :class:`pyre.patterns.AttributeClassifier.AttributeClassifier`

   Metaclass that inspects record declarations and endows their instances with the necessary
   infrastructure to support

   * named access of the fields in a record
   * composition via inheritance
   * derivations, i.e. fields whose values depend on the values of other fields

   .. method:: pyre_isMeasure(cls, field)
      :classmethod:


      Predicate that tests whether {field} is a measure


   .. method:: pyre_isDerivation(cls, field)
      :classmethod:


      Predicate that tests whether {field} is a derivation



.. py:class:: record

   Bases: :class:`pyre.framework.Dashboard.Dashboard`

   The base class for representing data extracted from persistent stores.

   Records have field descriptors that provide the information necessary to convert data
   between the representation used by the persistent store and the native python object
   required by the application.

   Records are similar to named tuples: the underlying storage mechanism is a tuple, and the
   fields are descriptors that provide named access to the tuple items. They are superior to
   named tuples since they enable the data model designer to specify types and constraints
   that must be satisfied by the data, and automate the conversion process to a large degree.

   Inheritance among {Record} subclasses is interpreted as composition: the set of fields that
   define a record is built out of the descriptors declared both locally and by all of its
   ancestors. Descriptor composition is subject to name shadowing.

   Records support {derivations}: fields whose value is computed using other record
   fields. Such fields are built automatically whenever a field declaration contains any sort
   of arithmetic on the right hand side.

   Details of the current implementation:

   * Storage for the record values is provided by {tuple}. This implies that indexed access
     using integers works as expected and does not require any special handling

   * Named access is handled through the field descriptors. Supporting composition via
     inheritance complicates the implementation a bit, as the rank of a given field is not
     known until the class mro is traversed and shadowing is taken into account. Each {Record}
     subclass maintains its own map from descriptor instances to the integer rank in the
     corresponding underlying tuple.

   .. attribute:: pyre_name
      

      

   .. attribute:: pyre_localFields
      

      

   .. attribute:: pyre_fields
      

      

   .. attribute:: pyre_measures
      

      

   .. attribute:: pyre_derivations
      

      

   .. attribute:: pyre_columns
      

      

   .. method:: pyre_immutable(cls, data=None, **kwds)
      :classmethod:


      Build a mutable instance


   .. method:: pyre_mutable(cls, data=None, **kwds)
      :classmethod:


      Build a mutable instance


   .. method:: pyre_selectColumns(cls, headers)
      :classmethod:


      Prepare a tuple of the column numbers needed to populate my instances, given a map
      (column name) -> (column index).

      This enables the managers of the various persistent stores to build record instances
      from a subset of the information they have access to. It is also designed to perform
      column name translations from whatever meta data is available in the store to the
      canonical record field names



.. py:class:: csv

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



