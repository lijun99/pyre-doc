:mod:`pyre.units.Parser`
========================

.. py:module:: pyre.units.Parser


Module Contents
---------------

.. py:class:: Parser(**kwds)

   Singleton that converts string representations of dimensional quantities into instances of
   Dimensional

   .. method:: parse(self, text, context=None)


      Convert the string representation in {text} into a dimensional quantity


   .. method:: _initializeContext(self)


      Build the initial list of resolvable unit symbols



