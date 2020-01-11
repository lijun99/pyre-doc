:mod:`pyre.components.CompatibilityReport`
==========================================

.. py:module:: pyre.components.CompatibilityReport


Module Contents
---------------

.. py:class:: CompatibilityReport(this, other, **kwds)

   Class that holds the assignment incompatibilities among configurables

   .. attribute:: this
      

      

   .. attribute:: other
      

      

   .. method:: isClean(self)
      :property:


      Check whether there are any incompatibilities to report


   .. method:: __bool__(self)


      Convert to True if no incompatibilities were reported



