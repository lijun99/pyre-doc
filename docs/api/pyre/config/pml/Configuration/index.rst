:mod:`pyre.config.pml.Configuration`
====================================

.. py:module:: pyre.config.pml.Configuration


Module Contents
---------------

.. py:class:: Configuration(parent, attributes, locator, **kwds)

   Bases: :class:`pyre.config.pml.Node.Node`

   Handler for the top level tag in pml documents

   .. attribute:: elements
      :annotation: = ['component', 'package', 'bind']

      

   .. method:: notify(self, parent, locator)


      Let {parent} now that processing this configuration tag is complete


   .. method:: assignment(self, event)


      Process the binding of a property to a value


   .. method:: conditionalAssignment(self, event)


      Process a binding of a property to a value



