:mod:`journal.Channel`
======================

.. py:module:: journal.Channel


Module Contents
---------------

.. py:class:: Channel(name, **kwds)

   Bases: :class:`pyre.patterns.Named.Named`

   This class encapsulates access to the shared channel state

   .. py:class:: Enabled

      Shared state for channels that are enabled by default

      .. attribute:: state
         :annotation: = True

         

      .. attribute:: device
         

         


   .. py:class:: Disabled

      Shared state for channels that are disabled by default

      .. attribute:: state
         :annotation: = False

         

      .. attribute:: device
         

         


   .. attribute:: journal
      

      

   .. attribute:: _index
      

      

   .. method:: active(self)
      :property:


      Get my current activation state


   .. method:: device(self)
      :property:


      Get my current output device


   .. method:: activate(self)


      Mark me as active


   .. method:: deactivate(self)


      Mark me as inactive


   .. method:: __bool__(self)


      Simplify the state testing



