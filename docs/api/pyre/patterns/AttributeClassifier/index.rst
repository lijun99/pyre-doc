:mod:`pyre.patterns.AttributeClassifier`
========================================

.. py:module:: pyre.patterns.AttributeClassifier


Module Contents
---------------

.. py:class:: AttributeClassifier

   Bases: :class:`pyre.patterns.AbstractMetaclass.AbstractMetaclass`

   A base metaclass that enables attribute categorization.

   A common pattern in pyre is to define classes that contain special attributes whose purpose
   is to collect declaration meta data and associate them with a class attribute. These
   attributes are processed by metaclasses and are converted into appropriate behavior. For
   example, components have properties, which are decorated descriptors that enable external
   configuration of component state. Similarly, XML parsing happens with the aid of classes
   that capture the syntax, semantics and processing behavior of tags by employing descriptors
   to capture the layout of an XML document.

   This class defines {pyre_harvest}, which scans the class attribute dictionary for instances
   of the special class {descriptor}. It also overrides {__prepare__} to provide attribute
   storage that records the order in which attributes were encountered in the class record.

   .. attribute:: pyre_reserved
      

      

   .. method:: __prepare__(cls, name, bases, **kwds)
      :classmethod:


      Build an attribute table that maintains a category index for attribute descriptors


   .. method:: pyre_harvest(cls, attributes, descriptor)
      :classmethod:


      Examine {attributes}, looking for instances of {descriptor}



