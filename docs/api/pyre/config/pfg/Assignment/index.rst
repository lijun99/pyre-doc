:mod:`pyre.config.pfg.Assignment`
=================================

.. py:module:: pyre.config.pfg.Assignment


Module Contents
---------------

.. py:class:: Assignment(token, **kwds)

   Bases: :class:`pyre.config.pfg.Event.Event`

   The resting place for key-value bindings

   .. attribute:: name
      

      

   .. attribute:: value
      

      

   .. attribute:: locator
      

      

   .. method:: bind(self, token)


      Extract my value from {token}


   .. method:: notify(self, parent)


      Tell my {parent} there is an assignment waiting



