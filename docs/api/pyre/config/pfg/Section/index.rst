:mod:`pyre.config.pfg.Section`
==============================

.. py:module:: pyre.config.pfg.Section


Module Contents
---------------

.. py:class:: Section(token, **kwds)

   Bases: :class:`pyre.config.pfg.EventContainer.EventContainer`

   The resting place for all scoped configuration events

   .. attribute:: name
      

      

   .. attribute:: family
      

      

   .. method:: assignment(self, event)


      Process an unconditional assignment


   .. method:: conditionalAssignment(self, event)


      Process a conditional assignment


   .. method:: notify(self, parent)


      Place my assignments in my parent's context



