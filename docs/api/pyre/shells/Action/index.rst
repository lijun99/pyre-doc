:mod:`pyre.shells.Action`
=========================

.. py:module:: pyre.shells.Action


Module Contents
---------------

.. py:class:: Action

   Bases: :class:`pyre.protocol`

   A protocol that facilitates application extensibility: components that implement {Action}
   can be invoked from the command line

   .. method:: main(self, *kwds)


      This is the implementation of the action


   .. method:: help(self, **kwds)


      Provide help with invoking this action


   .. method:: pyre_documentedActions(cls)
      :classmethod:


      Retrieve all visible implementations that are documented



