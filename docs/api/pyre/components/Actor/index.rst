:mod:`pyre.components.Actor`
============================

.. py:module:: pyre.components.Actor


Module Contents
---------------

.. py:class:: Actor(name, bases, attributes, *, family=None, **kwds)

   Bases: :class:`pyre.components.Requirement.Requirement`

   The metaclass of components

   {Actor} takes care of all the tasks necessary to convert a component declaration into a
   configurable entity that coöperates fully with the framework

   .. method:: pyre_name(self)
      :property:


      Return the component's family name


   .. method:: __call__(self, name=None, locator=None, globalAliases=False, **kwds)


      Build an instance of one of my classes


   .. method:: __setattr__(self, name, value)


      Trap attribute setting in my class record instances to support setting the default
      value using the natural syntax


   .. method:: __str__(self)



   .. method:: pyre_buildProtocol(cls, name, bases, implements)
      :classmethod:


      Build a class that describes the implementation requirements imposed on this
      {component}, given its class record and the list of protocols it {implements}



