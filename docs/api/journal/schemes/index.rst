:mod:`journal.schemes`
======================

.. py:module:: journal.schemes


Module Contents
---------------

.. py:class:: ColorScheme

   Bases: :class:`pyre.protocol`

   The color scheme protocol definition

   .. attribute:: header
      

      

   .. attribute:: body
      

      

   .. attribute:: filename
      

      

   .. attribute:: line
      

      

   .. attribute:: function
      

      

   .. attribute:: stackTrace
      

      

   .. attribute:: src
      

      

   .. attribute:: channel
      

      

   .. attribute:: debug
      

      

   .. attribute:: firewall
      

      

   .. attribute:: info
      

      

   .. attribute:: warning
      

      

   .. attribute:: error
      

      


.. py:class:: NoColor

   Bases: :class:`pyre.component`

   The base color scheme: no coloring

   .. attribute:: header
      

      

   .. attribute:: body
      

      

   .. attribute:: filename
      

      

   .. attribute:: line
      

      

   .. attribute:: function
      

      

   .. attribute:: stackTrace
      

      

   .. attribute:: src
      

      

   .. attribute:: channel
      

      

   .. attribute:: debug
      

      

   .. attribute:: firewall
      

      

   .. attribute:: info
      

      

   .. attribute:: warning
      

      

   .. attribute:: error
      

      


.. py:class:: DarkBackground

   Bases: :class:`journal.schemes.NoColor`

   A color scheme suitable for rendering in terminals with a dark background

   .. attribute:: header
      

      

   .. attribute:: body
      

      

   .. attribute:: filename
      

      

   .. attribute:: line
      

      

   .. attribute:: function
      

      

   .. attribute:: stackTrace
      

      

   .. attribute:: src
      

      

   .. attribute:: channel
      

      

   .. attribute:: debug
      

      

   .. attribute:: firewall
      

      

   .. attribute:: info
      

      

   .. attribute:: warning
      

      

   .. attribute:: error
      

      


.. py:class:: LightBackground

   Bases: :class:`journal.schemes.NoColor`

   A color scheme suitable for rendering in terminals with a dark background

   .. attribute:: header
      

      

   .. attribute:: body
      

      

   .. attribute:: filename
      

      

   .. attribute:: line
      

      

   .. attribute:: function
      

      

   .. attribute:: stackTrace
      

      

   .. attribute:: src
      

      

   .. attribute:: channel
      

      

   .. attribute:: debug
      

      

   .. attribute:: firewall
      

      

   .. attribute:: info
      

      

   .. attribute:: warning
      

      

   .. attribute:: error
      

      


.. data:: colors
   

   

.. data:: none
   

   

.. data:: dark
   

   

.. data:: light
   

   

