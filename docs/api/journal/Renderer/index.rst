:mod:`journal.Renderer`
=======================

.. py:module:: journal.Renderer


Module Contents
---------------

.. py:class:: Renderer

   Bases: :class:`pyre.protocol`

   The protocol specification that renderers must satisfy

   .. attribute:: ansi
      

      

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      Examine {sys.stdout} and turn on color output if the current terminal type supports it


   .. method:: render(self, text, metadata)


      Convert the diagnostic information into a form that a device can record



