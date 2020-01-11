:mod:`journal.Device`
=====================

.. py:module:: journal.Device


Module Contents
---------------

.. py:class:: Device

   Bases: :class:`pyre.protocol`

   The protocol that devices must implement

   .. attribute:: renderer
      

      

   .. attribute:: doc
      :annotation: = the formatting strategy

      

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The default {Device} implementation


   .. method:: record(self, page, metadata)


      Create a journal entry from the given information



