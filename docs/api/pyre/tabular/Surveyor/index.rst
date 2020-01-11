:mod:`pyre.tabular.Surveyor`
============================

.. py:module:: pyre.tabular.Surveyor


Module Contents
---------------

.. py:class:: Surveyor

   Bases: :class:`pyre.patterns.AttributeClassifier.AttributeClassifier`

   Inspect charts and harvest their dimensions

   .. method:: __prepare__(cls, name, bases, **kwds)
      :classmethod:


      Prepare a container for the attributes of a chart by looking through {kwds} for sheet
      aliases and making them available as class attributes during the chart
      declaration. This makes it possible to refer to sheets when setting up the chart
      dimensions



