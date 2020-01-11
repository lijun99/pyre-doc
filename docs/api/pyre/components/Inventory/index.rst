:mod:`pyre.components.Inventory`
================================

.. py:module:: pyre.components.Inventory


Module Contents
---------------

.. py:class:: Inventory(slots, **kwds)

   Bases: :class:`pyre.framework.Dashboard.Dashboard`

   Base class for the state storage strategies for component classes and instances

   .. attribute:: name
      

      

   .. attribute:: fragments
      :annotation: = []

      

   .. attribute:: package
      

      

   .. method:: initializeClass(cls)
      :classmethod:
      :abstractmethod:


      Build inventory for a component class


   .. method:: initializeInstance(cls)
      :classmethod:
      :abstractmethod:


      Build inventory for a component instance


   .. method:: getTraits(self)


      Return an iterable over my traits


   .. method:: getSlots(self)
      :abstractmethod:


      Return an iterable over the trait value storage


   .. method:: __getitem__(self, trait)



   .. method:: __setitem__(self, trait, item)



   .. method:: __iter__(self)




