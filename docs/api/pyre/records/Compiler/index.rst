:mod:`pyre.records.Compiler`
============================

.. py:module:: pyre.records.Compiler


Module Contents
---------------

.. py:class:: Compiler

   A strategy for pulling data from a stream and building {pyre.calc} nodes to represent both
   measures and derivations

   .. method:: __call__(self, record, source, **kwds)


      Pull values from {source} and build the associated nodes


   .. method:: onDescriptor(self, source, cache, descriptor)


      Handler for measures


   .. method:: onOperator(self, source, cache, operator)


      Handler for derivations


   .. method:: onLiteral(self, source, cache, literal)


      Handler for literals



