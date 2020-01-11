:mod:`pyre.traits.Behavior`
===========================

.. py:module:: pyre.traits.Behavior


Module Contents
---------------

.. py:class:: Behavior(method, tip=None, **kwds)

   Bases: :class:`pyre.traits.Trait.Trait`

   The base class for component methods that are part of its external interface

   .. attribute:: method
      

      

   .. attribute:: category
      :annotation: = behavior

      

   .. attribute:: isBehavior
      :annotation: = True

      

   .. method:: __get__(self, instance, cls)


      Access to the behavior


   .. method:: __set__(self, instance, value)


      Disable writing to behavior descriptors


   .. method:: __str__(self)




