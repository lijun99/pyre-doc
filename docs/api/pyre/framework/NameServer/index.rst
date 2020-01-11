:mod:`pyre.framework.NameServer`
================================

.. py:module:: pyre.framework.NameServer


Module Contents
---------------

.. py:class:: NameServer(name='pyre::nameserver', **kwds)

   Bases: :class:`pyre.calc.Hierarchical.Hierarchical`

   The manager of the full set of runtime objects that are accessible by name. This includes
   everything from configuration settings to components and interfaces

   .. method:: configpath(self)
      :property:


      Return an iterable over my configuration path


   .. method:: configurable(self, name, configurable, locator, priority=None)


      Add {configurable} to the model under {name}


   .. method:: package(self, name, executive, locator)


      Retrieve the named package from the model. If there is no such package, instantiate one,
      configure it, and add it to the model.


   .. method:: createPackage(self, name, locator)


      Build a new package node and attach it to the model


   .. method:: evaluate(self, expression)


      Evaluate the given {expression} in my current context


   .. method:: interpolate(self, expression)


      Interpolate the given {expression} in my current context


   .. method:: insert(self, value, priority, locator, key=None, name=None, split=None, factory=None)


      Add {value} to the store


   .. method:: retrieve(self, name)


      Retrieve the node registered under {name}. If no such node exists, an error marker will
      be built, stored in the symbol table under {name}, and returned.


   .. method:: __setitem__(self, name, value)


      Convert {value} into a node and update the model


   .. method:: store(self, key, name, node, info)


      Associate {name}, {node} and {info} with {key}


   .. method:: replace(self, key, name, oldNode, oldInfo, newNode, newInfo)


      Choose which settings to retain


   .. method:: pullGlobalIntoScope(self, scope, symbols)


      Merge settings for {traits} between global scope and the scope of {name}


   .. method:: __str__(self)


      Identify me by name



