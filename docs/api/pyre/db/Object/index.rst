:mod:`pyre.db.Object`
=====================

.. py:module:: pyre.db.Object


Module Contents
---------------

.. py:class:: Object

   Bases: :class:`pyre.framework.Dashboard.Dashboard`

   The base class of classes whose instances store part of their attributes in relational
   database tables.

   {Object} and its class {Persistent} provide the necessary layer to bridge object oriented
   semantics with the relational model. The goal is to make the existence of the relational
   tables more transparent to the developer of database applications by removing as much of
   the grunt work of storing and retrieving object state as possible.

   .. attribute:: pyre_extent
      

      

   .. attribute:: pyre_primaryTable
      

      


