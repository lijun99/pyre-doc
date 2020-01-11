:mod:`merlin.spells.About`
==========================

.. py:module:: merlin.spells.About


Module Contents
---------------

.. py:class:: About

   Bases: :class:`merlin.spell`

   Display information about this application

   .. attribute:: prefix
      

      

   .. attribute:: tip
      :annotation: = specify the portion of the namespace to display

      

   .. method:: copyright(self, plexus, **kwds)


      Print the copyright note of the merlin package


   .. method:: credits(self, plexus, **kwds)


      Print the acknowledgments


   .. method:: license(self, plexus, **kwds)


      Print the license and terms of use of the merlin package


   .. method:: nfs(self, plexus, **kwds)


      Dump the application configuration namespace


   .. method:: version(self, plexus, **kwds)


      Print the version of the merlin package


   .. method:: vfs(self, plexus, **kwds)


      Dump the application virtual filesystem



