:mod:`pyre.filesystem.InfoStat`
===============================

.. py:module:: pyre.filesystem.InfoStat


Module Contents
---------------

.. py:class:: InfoStat(info, **kwds)

   Mixin that knows how to pull information from {stat} structures

   .. attribute:: user
      

      

   .. attribute:: group
      

      

   .. attribute:: other
      

      

   .. attribute:: read
      

      

   .. attribute:: write
      

      

   .. attribute:: execute
      

      

   .. attribute:: masks
      

      

   .. method:: mode(self, entity=user, access=read)


      Determine whether {entity} has read permissions


   .. method:: dump(self, channel, indent='')


      Place the known information about this file in the given {channel}



