:mod:`pyre.calc.Postprocessor`
==============================

.. py:module:: pyre.calc.Postprocessor


Module Contents
---------------

.. py:class:: Postprocessor(postprocessor=identity().coerce, **kwds)

   A mix-in class that performs arbitrary transformations on the value of a node

   .. attribute:: _postprocessor
      

      

   .. method:: postprocessor(self)
      :property:


      Read access to my value post processor


   .. method:: getValue(self, **kwds)


      Intercept the node value retriever and make sure that the value the caller gets has
      been through my {postprocessor}



