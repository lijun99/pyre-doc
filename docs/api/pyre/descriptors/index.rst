:mod:`pyre.descriptors`
=======================

.. py:module:: pyre.descriptors


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Converter/index.rst
   Decorator/index.rst
   Descriptor/index.rst
   Normalizer/index.rst
   Processor/index.rst
   Public/index.rst
   Typed/index.rst
   Validator/index.rst
   exceptions/index.rst


Package Contents
----------------

.. py:class:: stem(optional=optional, input=input, output=output, level=level, **kwds)

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



.. py:class:: converter

   Bases: :class:`pyre.descriptors.Processor.Processor`

   A record method decorator that registers this method as a converter of descriptor values

   .. method:: __call__(self, method)


      Add {method} as a converter to my registered descriptors



.. py:class:: normalizer

   Bases: :class:`pyre.descriptors.Processor.Processor`

   A record method decorator that registers this method as a normalizer of descriptor values

   .. method:: __call__(self, method)


      Add {method} as a normalizer to my registered descriptors



.. py:class:: validator

   Bases: :class:`pyre.descriptors.Processor.Processor`

   A record method decorator that registers this method as a validator of descriptor values

   .. method:: __call__(self, method)


      Add {method} as a validator to my registered descriptors



.. py:class:: descriptor

   Bases: :class:`pyre.descriptors.Descriptor.Descriptor.variable`


.. data:: bool
   

   

.. data:: complex
   

   

.. data:: decimal
   

   

.. data:: float
   

   

.. data:: inet
   

   

.. data:: int
   

   

.. data:: identity
   

   

.. data:: str
   

   

.. data:: date
   

   

.. data:: dimensional
   

   

.. data:: path
   

   

.. data:: time
   

   

.. data:: timestamp
   

   

.. data:: uri
   

   

.. data:: array
   

   

.. data:: list
   

   

.. data:: set
   

   

.. data:: tuple
   

   

.. data:: istream
   

   

.. data:: ostream
   

   

.. function:: strings(default=list, **kwds)

   A list of strings


.. function:: uris(default=list, **kwds)

   A list of URIs


