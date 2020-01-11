:mod:`pyre.patterns.ExtentAware`
================================

.. py:module:: pyre.patterns.ExtentAware


Module Contents
---------------

.. py:class:: ExtentAware(name, bases, attributes, pyre_extentRoot=False, **kwds)

   Bases: :class:`pyre.patterns.AbstractMetaclass.AbstractMetaclass`

   Metaclass that endows its instances with awareness of their extent.

   The extent of a class is the set of its own instances and the instances of all of its
   subclasses.

   The class extent is stored with the first class that mentions {ExtentAware} as a metaclass,
   and all descendants are counted by that class. Descendants that want to keep track of their
   own extent and prevent their extent from being counted by their superclass must be declared
   with {pyre_extentRoot} set to {True}.

   implementation details:

       __new__: intercept the creation of the client class record and add the reference
       counting weak set as a class attribute

       __call__: capture the creation of an instance, since it is this method that triggers
       the call to the client class' constructor. we let super().__call__ build the instance
       and then add a weak reference to it in _pyre_extent

   .. method:: __call__(self, *args, **kwds)


      Intercept the call to the client constructor, build the instance and keep a weak
      reference to it



