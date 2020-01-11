:mod:`pyre.traits.Trait`
========================

.. py:module:: pyre.traits.Trait


Module Contents
---------------

.. py:class:: Trait

   Bases: :class:`pyre.descriptors.stem.variable`, :class:`pyre.framework.Dashboard.Dashboard`

   This is the base class for component features that form their public interface

   Traits extend the notion of a class attribute to an object that is capable of
   capturing information about the attribute that has no natural resting place as part of a
   normal class declaration.

   Traits enable end-user configurable state, for both simple attributes and references to
   more elaborate objects, such as other components. Individual inventory items need a name
   that enables access to the associated information, per-instance actual storage for the
   attribute value, and additional meta data, such as reasonable default values when the
   attribute is not explicitly given a value during configuration, and the set of constraints
   it should satisfy before it is considered a legal value.

   .. attribute:: category
      :annotation: = trait

      

   .. attribute:: isBehavior
      :annotation: = False

      

   .. attribute:: isProperty
      :annotation: = False

      

   .. attribute:: isFacility
      :annotation: = False

      

   .. attribute:: isConfigurable
      :annotation: = False

      

   .. method:: classConfigured(self, **kwds)


      Notification that the component class I am being attached to is configured


   .. method:: instanceConfigured(self, **kwds)


      Notification that the component instance I am being attached to is configured



