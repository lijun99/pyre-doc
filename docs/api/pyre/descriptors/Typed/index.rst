:mod:`pyre.descriptors.Typed`
=============================

.. py:module:: pyre.descriptors.Typed


Module Contents
---------------

.. py:class:: Typed(**kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   Mix-in class that encapsulates type information. Its instances participate in value
   conversions from external representations to python internal forms.

   .. attribute:: converters
      :annotation: = []

      

   .. attribute:: normalizers
      :annotation: = []

      

   .. attribute:: validators
      :annotation: = []

      

   .. method:: process(self, value, **kwds)


      Walk {value} through the steps from raw to validated


   .. method:: bind(self, **kwds)


      Called by my client to let me know that all the available meta-data have been harvested


   .. method:: listify(self, processors)


      Make sure {processors} is an iterable regardless of what the user left behind



