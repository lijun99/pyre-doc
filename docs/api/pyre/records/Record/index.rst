:mod:`pyre.records.Record`
==========================

.. py:module:: pyre.records.Record


Module Contents
---------------

.. py:class:: Record

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



