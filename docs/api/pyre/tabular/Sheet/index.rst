:mod:`pyre.tabular.Sheet`
=========================

.. py:module:: pyre.tabular.Sheet


Module Contents
---------------

.. py:class:: Sheet(name, **kwds)

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



