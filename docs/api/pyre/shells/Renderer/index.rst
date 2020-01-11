:mod:`pyre.shells.Renderer`
===========================

.. py:module:: pyre.shells.Renderer


Module Contents
---------------

.. py:class:: Renderer(**kwds)

   Bases: :class:`pyre.component`

   Custom replacement for the {journal} renderer

   .. attribute:: terminal
      

      

   .. attribute:: shortSeverities
      

      

   .. method:: render(self, page, metadata)


      Convert the diagnostic information into a form that a device can record


   .. method:: severityUpcase(self, metadata)


      Return an uppercased severity


   .. method:: severityShort(self, metadata)


      Return a three letter abbreviation for the severity



