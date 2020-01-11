:mod:`pyre.config.pfg.Event`
============================

.. py:module:: pyre.config.pfg.Event


Module Contents
---------------

.. py:class:: Event

   The abstract base class for all configuration event handlers

   .. attribute:: scopeSeparator
      :annotation: = .

      

   .. attribute:: fragmentSeparator
      :annotation: = #

      

   .. method:: notify(self, parent)
      :abstractmethod:


      Invoked when configuration data gathering is done for the active node and it is time to
      delegate any further processing to the containing node



