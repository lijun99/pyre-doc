:mod:`pyre.records.Evaluator`
=============================

.. py:module:: pyre.records.Evaluator


Module Contents
---------------

.. py:class:: Evaluator

   A strategy for pulling data from a stream, and performing evaluations and coercions as
   indicated by the field descriptors

   .. method:: __call__(self, record, source, **kwds)


      Pull values from {source}, perform the calculation encoded in the derivation expression
      graphs, walk values through coercions, and make the results available to the caller


   .. method:: onDescriptor(self, source, cache, descriptor)


      Handler for measures


   .. method:: onOperator(self, source, cache, operator)


      Handler for operators


   .. method:: onLiteral(self, source, cache, literal)


      Handler for descriptors that encapsulate foreign values



