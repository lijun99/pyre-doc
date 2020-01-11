:mod:`pyre.shells.ANSI`
=======================

.. py:module:: pyre.shells.ANSI


Module Contents
---------------

.. py:class:: ANSI(**kwds)

   Bases: :class:`pyre.component`

   A terminal that provides color capabilities using ANSI control sequences

   .. attribute:: ansi
      

      

   .. attribute:: x11
      

      

   .. attribute:: gray
      

      

   .. attribute:: misc
      

      

   .. method:: width(self)
      :property:


      Compute the width of the terminal


   .. method:: rgb(self, rgb, foreground=True)


      Mix the 6 digit hex string into an ANSI 24-bit color


   .. method:: rgb256(self, red=0, green=0, blue=0, foreground=True)


      Mix the three digit (r,g,b) base 6 string into an ANSI 256 color



