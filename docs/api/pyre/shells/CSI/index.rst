:mod:`pyre.shells.CSI`
======================

.. py:module:: pyre.shells.CSI


Module Contents
---------------

.. py:class:: CSI

   A generator of ANSI control strings

   .. method:: reset()
      :staticmethod:


      Reset all output attributes


   .. method:: csi3(bright=False, code=None)
      :staticmethod:


      Build an ANSI color sequence


   .. method:: csi8(red=0, green=0, blue=0, foreground=True)
      :staticmethod:


      Build an ANSI color sequence from the 256 color set, where each color can take a value in
      the interval [0, 5]


   .. method:: csi8_gray(gary=0, foreground=True)
      :staticmethod:


      Build an ANSI color sequence from the 8 bit color set that corresponds to a gray level in
      the range [0, 23]


   .. method:: csi24(red=0, green=0, blue=0, foreground=True)
      :staticmethod:


      Build an ANSI color sequence from the 24bit color set, where each color can take a value in
      the interval [0, 255]


   .. method:: blink(state=True)
      :staticmethod:


      Turn blink on or off



