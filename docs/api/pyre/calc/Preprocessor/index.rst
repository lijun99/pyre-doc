:mod:`pyre.calc.Preprocessor`
=============================

.. py:module:: pyre.calc.Preprocessor


Module Contents
---------------

.. py:class:: Preprocessor(preprocessor=identity().coerce, **kwds)

   A mix-in class that performs arbitrary transformations on the value of a node

   .. attribute:: preprocessor
      

      

   .. method:: setValue(self, value, **kwds)


      Hand the incoming {value} to my {preprocessor} before storing it



