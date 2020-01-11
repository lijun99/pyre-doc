:mod:`pyre.records.Accessor`
============================

.. py:module:: pyre.records.Accessor


Module Contents
---------------

.. py:class:: Accessor

   Bases: :class:`pyre.records.Selector.Selector`

   The object responsible for providing named access to field values

   Accessors connect the name of a field to its value in the underlying tuple by keeping track
   of the index of their column. This information is available when the record class is
   formed: accessors are built and attached to the tuple generators by {Templater}, the
   {Record} metaclass

   .. method:: __get__(self, record, cls)


      Field retrieval


   .. method:: __set__(self, record, value)


      Field modification



