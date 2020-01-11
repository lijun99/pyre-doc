:mod:`pyre.config.pml.Component`
================================

.. py:module:: pyre.config.pml.Component


Module Contents
---------------

.. py:class:: Component(parent, attributes, locator, **kwds)

   Bases: :class:`pyre.config.pml.Node.Node`

   Handler for the component tag in pml documents

   .. attribute:: elements
      :annotation: = ['component', 'bind']

      

   .. method:: notify(self, parent, locator)


      Transfer all the key,value bindings to my parent


   .. method:: assignment(self, event)


      Process a binding of a property to a value


   .. method:: conditionalAssignment(self, event)


      Process a conditional assignment



