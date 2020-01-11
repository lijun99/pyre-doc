:mod:`pyre.config.pml.Bind`
===========================

.. py:module:: pyre.config.pml.Bind


Module Contents
---------------

.. py:class:: Bind(parent, attributes, locator)

   Bases: :class:`pyre.config.pml.Node.Node`

   Handler for the bind tag in pml documents

   .. attribute:: elements
      :annotation: = []

      

   .. method:: content(self, text, locator)


      Store the value of the key


   .. method:: notify(self, parent, locator)


      Let {parent} now that processing this bind tag is complete



