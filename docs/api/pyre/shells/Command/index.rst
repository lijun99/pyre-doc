:mod:`pyre.shells.Command`
==========================

.. py:module:: pyre.shells.Command


Module Contents
---------------

.. py:class:: Command(name, spec, plexus, **kwds)

   Bases: :class:`pyre.component`

   A component that implements {Action}

   .. attribute:: dry
      

      

   .. attribute:: doc
      :annotation: = show what would get done without actually doing anything

      

   .. attribute:: pyre_spec
      

      

   .. method:: main(self, plexus, **kwds)


      This is the implementation of the action


   .. method:: help(self, plexus, **kwds)


      Show a help screen


   .. method:: __call__(self, plexus, argv)


      Commands are callable


   .. method:: pyre_help(self, spec, indent=' ' * 4, **kwds)


      Hook for the application help system



