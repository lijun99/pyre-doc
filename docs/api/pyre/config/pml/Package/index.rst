:mod:`pyre.config.pml.Package`
==============================

.. py:module:: pyre.config.pml.Package


Module Contents
---------------

.. py:class:: Package(parent, attributes, locator, **kwds)

   Bases: :class:`pyre.config.pml.Node.Node`

   Handler for the package tag in pml documents

   .. attribute:: elements
      :annotation: = ['component', 'package', 'bind']

      

   .. method:: notify(self, parent, locator)


      Transfer all the key,value bindings to my parent


   .. method:: assignment(self, event)


      Process a binding of a property to a value


   .. method:: conditionalAssignment(self, event)


      Process a conditional assignment



