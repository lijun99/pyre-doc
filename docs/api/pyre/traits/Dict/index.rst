:mod:`pyre.traits.Dict`
=======================

.. py:module:: pyre.traits.Dict


Module Contents
---------------

.. py:class:: Dict(schema=Property.identity(), default=object, **kwds)

   Bases: :class:`pyre.traits.Slotted.Slotted`

   A property that maps strings to components

   .. attribute:: typename
      :annotation: = dict

      

   .. method:: macro(self)
      :property:


      The default strategy for handling slot values that are strings and therefore subject to
      some kind of evaluation in the context of the configuration store


   .. method:: native(self, value, **kwds)


      The default strategy for handling macros in slot values


   .. method:: process(self, value, **kwds)


      Walk {value} through the casting procedure appropriate for clients that are component
      classes


   .. method:: instantiate(self, value, **kwds)


      Walk {value} through the casting procedure appropriate for clients that are component
      instances


   .. method:: classConfigured(self, component, **kwds)


      Notification that the client class record has been configured


   .. method:: instanceConfigured(self, instance, **kwds)


      Notification that the client class record has been configured


   .. method:: catalog(self, factory, value, node, **kwds)


      Instantiate and initialize an appropriate map


   .. method:: configureClient(self, client, myFactory, traitFactory)


      A named client with public inventory requires further configuration



.. py:class:: Map(schema, factory, *args, **kwds)

   Bases: :class:`collections.abc.MutableMapping`, :class:`pyre.framework.Dashboard.Dashboard`

   The base class for the storage helpers

   .. attribute:: schema
      

      

   .. attribute:: factory
      

      

   .. attribute:: map
      

      

   .. method:: __delitem__(self, name)


      Remove {name} from my map


   .. method:: __iter__(self)


      Create an iterator over my map


   .. method:: __len__(self)


      Compute my size


   .. method:: __contains__(self, name)


      Check whether {name} is in my map


   .. method:: __setitem__(self, name, value)


      Store {value} in the map under {name}


   .. method:: __str__(self)


      Build a simple string representation of my contents



.. py:class:: KeyMap(key, *args, **kwds)

   Bases: :class:`pyre.traits.Dict.Map`

   A storage strategy that is appropriate when a client has public inventory

   .. method:: __getitem__(self, name)


      Retrieve the value associated with {name} and convert according to my schema


   .. method:: insert(self, name, value, priority, locator)


      Store {value} in the map under {name}



.. py:class:: NameMap

   Bases: :class:`pyre.traits.Dict.Map`

   A storage strategy for nameless clients

   .. method:: __getitem__(self, name)


      Retrieve the value associated with {name} and convert according to my schema


   .. method:: insert(self, name, value, **kwds)


      Build a slot to hold {value} and place it in the map



