:mod:`pyre.db.Selector`
=======================

.. py:module:: pyre.db.Selector


Module Contents
---------------

.. py:class:: Selector

   Bases: :class:`pyre.records.templater`

   Metaclass that inspects a query declaration and collects the information necessary to build
   the corresponding SELECT expressions

   .. attribute:: pyre_reserved
      

      

   .. method:: __prepare__(cls, name, bases, hidden=False, **kwds)
      :classmethod:


      Build an attribute table that contains the local table aliases



