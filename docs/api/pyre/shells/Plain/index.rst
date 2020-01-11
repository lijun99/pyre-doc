:mod:`pyre.shells.Plain`
========================

.. py:module:: pyre.shells.Plain


Module Contents
---------------

.. py:class:: Plain

   Bases: :class:`pyre.component`

   A terminal that provides no color capabilities

   .. attribute:: ansi
      

      

   .. attribute:: x11
      

      

   .. attribute:: gray
      

      

   .. attribute:: misc
      

      

   .. method:: width(self)
      :property:


      Compute the width of the terminal


   .. method:: rgb(self, **kwds)


      The 24-bit color request


   .. method:: rgb256(self, red=0, green=0, blue=0, foreground=True)


      The 256-color palette request



