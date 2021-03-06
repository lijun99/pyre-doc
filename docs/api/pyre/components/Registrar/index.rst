:mod:`pyre.components.Registrar`
================================

.. py:module:: pyre.components.Registrar


Module Contents
---------------

.. py:class:: Registrar(**kwds)

   The manager of protocols, component classes and their instances

   All user defined protocols and components are registered with {Registrar} as they
   are encountered by the framework. Clients can discover the protocol and component classes
   that are registered, the set of instances of any component, as well as the components that
   implement a particular protocol.

   The two base classes {pyre.components.Protocol} and {pyre.components.Component}, as well
   as the protocol specifications autogenerated by {Role}, are declared with the special
   attribute {internal} set to {True} and they are not registered.

   .. attribute:: protocols
      

      

   .. attribute:: components
      

      

   .. attribute:: implementers
      

      

   .. method:: registerNamingServer(self, server)


      Register {server} as a naming serice


   .. method:: registerProtocolClass(self, protocol)


      Register the {protocol} class record


   .. method:: registerComponentClass(self, component)


      Register the {component} class record


   .. method:: registerComponentInstance(self, instance)


      Register this component instance


   .. method:: nameInstance(self, componentClass)


      Attempt to generate a name for an instance of {componentClass}


   .. method:: observeProtocols(self, observer)


      Add {observer} to the set of entities interested in the registration of new protocols


   .. method:: observeComponents(self, observer)


      Add {observer} to the set of entities interested in the registration of new components


   .. method:: observeInstances(self, observer)


      Add {observer} to the set of entities interested in the registration of new instances


   .. method:: publicProtocols(self)


      Generate a topologically sorted sequence of registered public protocols


   .. method:: publicImplementers(self, protocol)


      Generate a sequence of public components that implement the given {protocol}


   .. method:: findRegisteredProtocols(self, component)


      Build a sequence of the registered protocols that are implemented by this component


   .. method:: retrieveComponentByName(self, componentClass, name)


      Look through the registered instances of {componentClass} for one with the given {name}


   .. method:: depthFirst(self, configurable, visited)


      Workhorse for the protocol traversal in topologically sorted order



