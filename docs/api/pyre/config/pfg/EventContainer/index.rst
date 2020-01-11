:mod:`pyre.config.pfg.EventContainer`
=====================================

.. py:module:: pyre.config.pfg.EventContainer


Module Contents
---------------

.. py:class:: EventContainer(**kwds)

   Bases: :class:`pyre.config.pfg.Event.Event`

   The abstract base class of all containers of configuration events

   .. attribute:: assignments
      

      

   .. attribute:: conditionalAssignments
      

      

   .. method:: assignment(self, event)


      Process an unconditional assignment


   .. method:: conditionalAssignment(self, event)


      Process a conditional assignment



