:mod:`pyre.patterns.Singleton`
==============================

.. py:module:: pyre.patterns.Singleton


Module Contents
---------------

.. py:class:: Singleton

   Bases: :class:`pyre.patterns.AbstractMetaclass.AbstractMetaclass`

   Provide support for classes that create and manage a single instance

   Adapted from Michele Simionato's implementation

   .. method:: __call__(cls, **kwds)


      Build and return the singleton instance every time the constructor is called



