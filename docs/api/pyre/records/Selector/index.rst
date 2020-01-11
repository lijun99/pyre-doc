:mod:`pyre.records.Selector`
============================

.. py:module:: pyre.records.Selector


Module Contents
---------------

.. py:class:: Selector(index, field, **kwds)

   The base class for objects responsible for providing named access to field descriptors

   .. attribute:: index
      

      

   .. attribute:: field
      

      

   .. method:: __get__(self, record, cls)


      Field retrieval


   .. method:: __set__(self, record, value)
      :abstractmethod:


      Field modification



