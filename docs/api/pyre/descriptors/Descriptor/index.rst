:mod:`pyre.descriptors.Descriptor`
==================================

.. py:module:: pyre.descriptors.Descriptor


Module Contents
---------------

.. py:class:: Descriptor(optional=optional, input=input, output=output, level=level, **kwds)

   The base class for typed descriptors

   Descriptors are class data members that collect compile time meta-data about attributes.

   In pyre, classes that use descriptors typically have a non-trivial metaclass that harvests
   them and catalogs them. The base class that implements most of the harvesting logic is
   {pyre.patterns.AttributeClassifier}. The descriptors themselves are typically typed,
   because they play some kind of rôle during conversions between internal and external
   representations of data.

   .. py:class:: variable

      Concrete class for representing descriptors

      .. attribute:: category
         :annotation: = descriptor

         

      .. method:: identify(self, authority, **kwds)


         Let {authority} know I am a descriptor



   .. attribute:: level
      :annotation: = 0

      

   .. attribute:: input
      :annotation: = False

      

   .. attribute:: output
      :annotation: = False

      

   .. attribute:: optional
      :annotation: = True

      

   .. method:: bind(self, **kwds)


      Called by my client to let me know that all the available meta-data have been harvested



