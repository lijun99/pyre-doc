:mod:`pyre.records.Templater`
=============================

.. py:module:: pyre.records.Templater


Module Contents
---------------

.. py:class:: Templater(name, bases, attributes, **kwds)

   Bases: :class:`pyre.patterns.AttributeClassifier.AttributeClassifier`

   Metaclass that inspects record declarations and endows their instances with the necessary
   infrastructure to support

   * named access of the fields in a record
   * composition via inheritance
   * derivations, i.e. fields whose values depend on the values of other fields

   .. method:: pyre_isMeasure(cls, field)
      :classmethod:


      Predicate that tests whether {field} is a measure


   .. method:: pyre_isDerivation(cls, field)
      :classmethod:


      Predicate that tests whether {field} is a derivation



