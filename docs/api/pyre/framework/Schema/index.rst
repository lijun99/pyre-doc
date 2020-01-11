:mod:`pyre.framework.Schema`
============================

.. py:module:: pyre.framework.Schema


Module Contents
---------------

.. py:class:: Schema(executive, **kwds)

   The singleton that indexes the database schema of a pyre application

   .. attribute:: models
      

      

   .. method:: dependencies(self)


      Build a graph of tables and their dependencies


   .. method:: sort(self)


      Visit tables in topological order


   .. method:: _sort(self, table, done)


      The engine of the topological sort



