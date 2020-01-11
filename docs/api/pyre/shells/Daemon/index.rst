:mod:`pyre.shells.Daemon`
=========================

.. py:module:: pyre.shells.Daemon


Module Contents
---------------

.. py:class:: Daemon

   Bases: :class:`pyre.shells.Fork.Fork`

   A shell that turns a process into a daemon, i.e. a process that is detached from its
   parent and has no access to a terminal

   .. attribute:: capture
      

      

   .. attribute:: doc
      :annotation: = control whether to create communication channels to the daemon process

      

   .. attribute:: model
      

      

   .. attribute:: doc
      :annotation: = the programming model

      

   .. attribute:: daemon
      

      

   .. attribute:: doc
      :annotation: = internal marker to indicate that the spawning is complete

      

   .. method:: launch(self, application, *args, **kwds)


      Invoke the application behavior

      For daemons, this is somewhat involved: the process forks twice in order to detach
      itself completely from its parent.



