:mod:`pyre.components.Role`
===========================

.. py:module:: pyre.components.Role


Module Contents
---------------

.. py:class:: Role(name, bases, attributes, *, family=None, **kwds)

   Bases: :class:`pyre.components.Requirement.Requirement`

   The metaclass for protocols

   .. method:: pyre_name(self)
      :property:


      The protocol's name is its family name


   .. method:: __call__(self, **kwds)


      The instantiation of protocol objects creates facility descriptors


   .. method:: __str__(self)



   .. method:: facility(self, **kwds)


      Build my trait descriptor



