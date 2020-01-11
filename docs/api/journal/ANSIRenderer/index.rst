:mod:`journal.ANSIRenderer`
===========================

.. py:module:: journal.ANSIRenderer


Module Contents
---------------

.. py:class:: ANSIRenderer(**kwds)

   Bases: :class:`pyre.component`

   A color capable text renderer

   .. attribute:: header
      

      

   .. attribute:: doc
      :annotation: = the marker to use while rendering the diagnostic metadata

      

   .. attribute:: body
      

      

   .. attribute:: doc
      :annotation: = the marker to use while rendering the diagnostic body

      

   .. attribute:: scheme
      

      

   .. attribute:: doc
      :annotation: = the set of colors to use when rendering diagnostics

      

   .. attribute:: esc
      :annotation: = [{}m

      

   .. attribute:: colors
      

      

   .. method:: render(self, page, metadata)


      Convert the diagnostic information into a form that a device can record



