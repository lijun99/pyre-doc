:mod:`pyre.tracking.Script`
===========================

.. py:module:: pyre.tracking.Script


Module Contents
---------------

.. py:class:: Script(source, line=None, function=None)

   A locator that records information relevant to python scripts. This information is
   typically extracted from stack traces so it contains whatever can be harvested by
   introspection

   .. attribute:: __slots__
      :annotation: = ['source', 'line', 'function']

      

   .. method:: __str__(self)




